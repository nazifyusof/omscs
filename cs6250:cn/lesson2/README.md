# Lesson 2: Transport and Application Layers

## Intro
According to this model, the network layer makes the best effort to deliver data packets. Thus, it does not guarantee the delivery of packets, nor does it guarantee the integrity of the data. So, here is where the transport layer comes to offer some of these functionalities. The transport layer allows application programmers to develop applications assuming a standard set of functionalities provided by the transport layer. So the applications can run over diverse networks regardless of different network interfaces or possible unreliability of the network.

Two most common transport protocols are:
1. TCP 
2. UDP

---

## Key concepts:
* The role of the transport layer above IP
* Application-to-application communication
* UDP versus TCP
* Multiplexing and demultiplexing with ports and sockets
* TCP connection establishment and teardown
* Reliable delivery, sequence numbers, ACKs, and retransmissions
* Fast retransmit and duplicate ACKs
* Flow control and the receive window
* Congestion control and the congestion window
* Slow start, congestion avoidance, AIMD, and TCP CUBIC

---

## Segment
- The sockets are identified based on special fields (shown below) in the segment such as the source port number field and the destination port number field.
![img.png](image/img.png)

---

## Multiplexing
- Ability for a host to run multiple applications to use the network simultaneously.
  - E.g. Person using Facebook and Spotify at the same time on the same device. Network has only one IP address, but additional identifiers known as **port** numbers allow the network to deliver data to the correct application.
- the sending host will need to gather data from different sockets and encapsulate each data chunk with header information (that will later be used in demultiplexing) to create segments, and then forward the segments to the network layer
- Two types of multiplexing:
  - Connectionless
  - Connection-oriented

---

## De-multiplexing
- The job of delivering the data included in the transport-layer segment to the appropriate socket, as defined in the segment fields,

---

## Connectionless Multiplexing and De-multiplexing
- The identifier of a UDP socket is a **two-tuple** that consists of a destination IP address and a destination port number.
- Suppose that Host A sends data to Host B. The transport layer in Host A creates a transport-layer segment with the application data, the source port, and the destination port, and then Host A forwards the segment to the network layer. In turn, the network layer encapsulates the segment into a network-layer datagram and sends it to Host B with best-effort delivery
- Let’s suppose that the datagram is successfully received by Host B. The transport layer at host B identifies the correct socket by looking at the field of the destination port. In the case host B runs multiple processes, each process will have its own UDP socket and, therefore, a distinct associated port number. Host B will use this information to demultiplex the receiving data to the correct socket. Suppose Host B receives UDP segments with a specific destination port number. In that case, it will forward the segments to the same destination process via the same destination socket, even if the segments come from different source hosts or source port numbers.

![img_1.png](image/img_1.png)


---

## Connection-oriented Multiplexing and De-multiplexing
- The identifier for a TCP socket is a **four-tuple** that consists of the source IP, source port, destination IP, and destination port.
- The TCP server has a listening socket that waits for connection requests coming from TCP clients. A TCP client creates a socket and sends a connection request, which is a TCP segment that has a source port number chosen by the client, a destination port number 12000, and a special connection-establishment bit set in the TCP header. Finally, the TCP server receives the connection request and creates a socket identified by the four-tuple source IP, source port, destination IP, and destination port. 
- The server uses this socket identifier to demultiplex incoming data and forward them to this socket. Now, the TCP connection is established, and the client and server can send and receive data between one another.   
![img_2.png](image/img_2.png)
![img_3.png](image/img_3.png)
- In this example, we have three hosts: A, B, and C. Host C initiates two HTTP sessions to server B, while Host A initiates one HTTP session to server B. 
- Hosts C and A assign port numbers to their connections independently of one another. Host C assigns port numbers 26145 and 7532.
- If Host A assigns the same port number as C, Host B can still demultiplex incoming data from the two connections because the connections are associated with different source IP addresses.

### Extra Notes:
- Let's assume we have a web server listening for connection requests on port 80. Clients send their initial connection requests and subsequent data with destination port 80. The web server can demultiplex incoming data based on their unique source IP addresses and source port numbers.
- The client and the server may be using persistent HTTP sessions, in which case they exchange HTTP messages via the same server socket.
- The client and the server may be using a non-persistent HTTP session, where for every request and response, a new TCP connection and a new socket are created and closed for every response/request. 
  - A busy web server may experience severe performance impact.

---

## UDP Protocol
- UDP is an unreliable protocol that lacks the mechanisms that TCP has. It is a **connectionless** protocol that does not require the establishment of a connection (e.g., the three-way handshake) before sending packets.
- Pros:
  - fewer delays 
  - better control over sending data
- UDP has no congestion control or similar mechanisms.
  - As soon as the application passes data to the transport layer, UDP encapsulates it and sends it over to the network layer.
  - In contrast, TCP “intervenes” with a congestion-control mechanism or retransmission of unacknowledged packets. These TCP mechanisms cause further delays.
- UDP has no connection management overhead
  - We will see that TCP uses a three-way handshake before it begins transferring data. 
  - UDP forgoes the connection and starts sending data immediately. The lack of connection establishment and maintenance means even fewer delays will occur.
![img_4.png](image/img_4.png)

- UDP has 64-bit header consisting of
  - Source port number 
  - Destination port number 
  - Length of the UDP segment (header and data). 
  - Checksum (an error checking mechanism): provides a basic error checking since there is no guarantee for link-by-link reliability. **The UDP sender adds the bits of the source port, the destination port, the packet length and the application data**. It performs a 1's complement on the sum (all 0s are turned to 1 and all 1s are turned to 0s), which is the value of the checksum. The receiver adds all the four 16-bit words (including the checksum). The result should be all 1's unless an error has occurred
![img_5.png](image/img_5.png)

---

## The TCP Three-Way Handshake
- Connection Establishment
1. Step 1: The TCP client sends a special segment (containing no data) with the SYN bit set to 1. The client also generates an initial sequence number (client_isn) and includes it in this special TCP SYN segment.
2. Step 2: The server, upon receiving this packet, allocates the required resources for the connection and sends back the special "connection-granted" segment which we call SYNACK segment. This packet has the SYN bit set to 1, the acknowledgement field of the TCP segment header set to client_isn+1, and a randomly chosen initial sequence number (server_isn) for the server.
3. Step 3: When the client receives the SYNACK segment, it also allocates buffer and resources for the connection and sends an acknowledgment with SYN bit set to 0.
![img_6.png](image/img_6.png)


- Connection Teardown
1. Step 1: When the client wants to end the connection, it sends a segment with FIN bit set to 1 to the server. 
2. Step 2: The server acknowledges that it has received the connection closing request and is now working on closing the connection. 
3. Step 3: The server then sends a segment with FIN bit set to 1, indicating that connection is closed. 
4. Step 4: The client sends an ACK for it to the server. It also waits for sometime to resend this acknowledgment in case the first ACK segment is lost.
![img_7.png](image/img_7.png)


---

## Reliable Transmission
- Network layer is unreliable, and this may lead to packets being lost or arriving out of order. This can be an issue for a lot of applications. For example, a file downloaded over the Internet might become corrupted if some packets become lost during the transfer.
- **TCP guarantees in-order delivery** of the application-layer data without any loss or corruption

### How?
- the sender should be able to know which segments were received by the remote host and which were lost by
  - Automatic Repeat Request or ARQ: having the receiver send acknowledgments indicating that it has successfully received the specific segment. If the sender does not receive an acknowledgment within a given period of time, the sender can assume the packet is lost and resend it
  - Stop and Wait ARQ: The simplest way would be for the sender to send a packet and wait for its acknowledgment from the receiver.
    - Note that the algorithm typically needs to figure out the waiting time after which it resends the packet, and this estimation can be tricky. A small timeout value can lead to unnecessary retransmissions, but a large timeout value can lead to unnecessary delays. Typically the timeout value is a function of the estimated **round trip time (RTT)** of the connection.
- This type of alternate sending and waiting for acknowledgment has a significantly low performance. To solve this problem, the sender can send multiple packets without waiting for acknowledgments. More specifically, the sender may send at most N unacknowledged packets typically referred to as the **window size**. As the sender receives an acknowledgment from the receiver, it can send more packets based on the window size. In implementing this, we need to take care of the following concerns:
  - The receiver needs to identify and notify the sender of a missing packet. Thus, each packet is tagged with a unique byte sequence number which is increased for subsequent packets in the flow based on the size of the packet.
  -  Also, both sender and receiver would need to buffer more than one packet. For instance, the sender would need to buffer packets that have been transmitted but not acknowledged. Similarly, the receiver may need to buffer packets because the rate of consuming these packets (e.g., writing to a disk) is slower than the rate at which the packets arrive.

### Receiver Notifies Sender of Missing Packets
1. One way is for the receiver to send an ACK for the most recently received in-order packet. The sender would then send all packets from the most recently received in-order packet, even if some of them had been sent before. The receiver can simply discard any out-of-order received packets. This is called Go-back-N. In the figure below, packet 7 is lost in the network so the receiver will discard any subsequent packets. The sender will send all the packets starting from 7 again. 

Clearly, in the above case, a single packet error can cause a lot of unnecessary retransmissions

![img_8.png](image/img_8.png)

2. TCP uses **selective ACKing**.  The sender retransmits only those packets that it suspects were received in error. Then, the receiver would acknowledge a correctly received packet even if it is not in order. The out-of-order packets are buffered until any missing packets have been received, at which point the batch of the packets can be delivered to the application layer. Note that, even in this case, TCP would need to use a timeout as there is a possibility of ACKs getting lost in the network.

In addition to using a timeout to detect loss of packets, TCP also uses duplicate acknowledgments as a means to detect packet loss. A duplicate ACK is an additional acknowledgment of a segment for which the sender has already received acknowledgment earlier. When the sender receives 3 duplicate ACKs for a packet, it considers the packet to be lost and will retransmit it instead of waiting for the timeout. This is known as **fast retransmit**. For example, in the figure below, once the sender receives 3 duplicate ACKs, it will retransmit packet 7 without waiting for a timeout.

![img_9.png](image/img_9.png)


---

## Transmission Control
- Why control the transmission rate?
- Where should the transmission control function reside in the network stack?  
  - Turns out that transmission control is a fundamental function for most applications. Therefore implementing it in the transport layer is easier.

---

## Flow Control
- Flow control: Controlling the Transmission Rate to Protect the Receiver buffer
- It helps match the sender’s rate against the receiver’s rate of reading the data
- In addition, the sender maintains a variable receive window rwnd. It provides the sender an idea of how much data the receiver can handle at the moment.
- Why?
  - protect the receiver buffer from overflowing
    - Recall that TCP uses a buffer at the receiver end to buffer packets that have not been transmitted to the application. The receiver might be involved with multiple processes and does not read the data instantly. This can cause the accumulation of a massive amount of data and overflow the receive buffer.
- Example
  - Consider two hosts, A and B, communicating with each other over a TCP connection. Host A wants to send a file to Host B. Host B allocates a receive buffer of size RcvBuffer to this connection. The receiving host maintains two variables:
    - LastByteRead: the number of the last bytes in the data stream read from the buffer by the application process in B
    - LastByteRcvd: the number of the last bytes in the data stream that has arrived from the network and has been placed in the receive buffer at B
  - to not overflow the buffer, TCP needs to make sure that `LastByteRcvd` - `LastByteRead` <= `RcvBuffer`
  - The extra space that the receive buffer has is specified using a parameter termed as receive window. `rwnd = RcvBuffer - [LastByteRcvd - LastByteRead]`
- The receiver advertises the value `rwnd` in every segment/ACK it sends back to the sender.
- The sender keeps track two vars
  - LastByteSent
  - LastByteAcked
- `UnACKed Data Sent = LastByteSent - LastByteAcked`
- To not overflow the receiver’s buffer, the sender must ensure that the maximum number of unacknowledged bytes it sends is no more than the `rwnd`. Thus we need
  - `LastByteSent – LastByteAcked  <= rwnd`
- Caveat:
  - Consider a scenario where the receiver had informed the sender that rwnd = 0, and thus the sender stops sending data. Also, assume that B has nothing to send to A. Now, as the application processes the data at the receiver, the receiver buffer is cleared. Still, the sender may never know that new buffer space is available and will be blocked from sending data even when the receiver buffer is empty.
  - TCP resolves this problem by making the sender **continue sending segments of size 1** byte even after rwnd = 0. When the receiver acknowledges these segments, it will specify the rwnd value, and the sender will know as soon as the receiver has some room in the buffer.

![img_10.png](image/img_10.png)

---

## Congestion Control Introduction
- Congestion control: Controlling the transmission rate to  protect the network from congestion

### Goals
  - Efficiency. We should get high throughput, or utilization of the network should be high.
  - Fairness. Each user should have their fair share of the network bandwidth. The notion of fairness is dependent on the network policy. For this context, we will assume that every flow under the same bottleneck link should get equal bandwidth.
  - Low delay. In theory, it is possible to design protocols with consistently high throughput assuming infinite buffer. Essentially, we could keep sending the packets to the network, and they will get stored in the buffer and eventually get delivered. However, it will lead to long queues in the network leading to delays. Thus, applications sensitive to network delays such as video conferencing will suffer. Therefore, we want the network delays to be minor.
  - Fast convergence. The idea here is that a flow should converge to its fair allocation fast. Fast convergence is crucial since a typical network’s workload is composed of many short flows and few long flows. If the convergence to fair share is not fast enough, the network will still be unfair for these short flows.

### Approaches
- There are **two approaches**
  - network-assisted congestion control
    - we rely on the network layer to provide explicit feedback to the sender about congestion in the network
    - For instance, routers could use an ICMP source quench to notify the source that the network is congested. However, even the ICMP packets could be lost under severe congestion, rendering the network feedback ineffective.
  - end-to-end congestion control
    - the network here does not provide any explicit feedback about congestion to the end hosts. Instead, the hosts infer congestion from the network behavior and adapt the transmission rate.
- Eventually, TCP ended up using the end-to-end approach because it largely aigns with the end-to-end principle of the Internet architecture
- Congestion control is a primitive provided in the transport layer, whereas routers operate at the network layer. Therefore, the feature resides in the end nodes with no support from the network. Note that this is no longer true as certain routers in the modern networks can provide explicit feedback to the end-host by using protocols such as ECNLinks to an external site. and QCNLinks to an external site..

### Signs of Congestion
- Two main signals
  - packet delay
    - the queues in the router buffers build-up, leading to increased packet delays
    - Thus, an increase in the round trip time, which can be estimated based on ACKs, can indicate congestion in the network.
    - However, it turns out that packet delays in a network tend to be variable, making delay-based congestion inference quite tricky
  - packet loss
    - As the network gets congested, routers start dropping packets.
    - Note that packets can also be lost due to other reasons such as routing errors, hardware failure, time-to-live (TTL) expiry, error in the links, or flow control problems, although it is rare.
- The earliest implementation of TCP used packet loss as a signal for congestion. This is mainly because TCP already detected and handled packet losses to provide reliability.

### How TCP Sender Limit The Sending Rate?
- TCP congestion control is to
  - determine the network's available capacity
  - choose how many packets to send without adding to the network's congestion level.
- TCP uses a congestion window similar to the receive window used for flow control. It represents the maximum number of unacknowledged data that a sending host can have in transit (sent but not yet acknowledged).
- TCP uses a **probe-and-adapt** approach in adapting the congestion window. Under normal conditions, TCP increases the congestion window trying to achieve the available throughput. Once it detects congestion, the congestion window is decreased.
- In the end, the number of unacknowledged data that a sender can have is the minimum between the congestion window and the receive window.
  - `LastByteSent – LastByteAcked <= min{cwnd, rwnd}`
- In a nutshell, a TCP sender cannot send faster than the slowest component, which is either the network or the receiving host.

### Congestion Control at TCP - AIMD
- additive increase/multiplicative decrease (AIMD): It decreases the window when the level of congestion goes up, and it increases the window when the level of congestion goes down
- AIMD approach reduces the congestion window at a much faster rate than it increases the congestion window
- The main reason for this approach is that the consequences of having too large a window are much worse than those of it being too small.
- For example, when the window is too large, more packets will be dropped and retransmitted, making network congestion even worse; thus, it is crucial to reduce the number of packets being sent into the network as quickly as possible.
- Additive Increase
  - The connection starts with a constant initial window, typically 2, and increases it additively.
  -  The idea behind additive increase is to increase the window by one packet every RTT (Round Trip Time). So, in the additive increase part of the AIMD, every time the sending host successfully sends a CongestionWindow (`cwnd`) number of packets it adds 1 to `cwnd`
  - Also, in practice, this increase in AIMD happens incrementally. TCP does not wait for ACKs of all the packets from the previous RTT. Instead, it increases the congestion window size as soon as each ACK arrives. In bytes, this increment is a portion of the MSS (Maximum Segment Size).
  - `Increment = MSS × (MSS / CongestionWindow)`
  - `CongestionWindow += Increment`
  - ![img_11.png](image/img_11.png)
- Multiplicative Decrease
  - Once TCP detects congestion, it reduces the rate at which the sender transmits.
  - When the TCP sender detects that a loss event has occurred, then it sets `cwnd` to half of its previous value.
  - For example, suppose the `cwnd` is currently set to 16 packets. If a loss is detected, then cwnd is set to 8. 
  - Further losses would result in the `cwnd` to be reduced to 4, and then to 2, and then to 1
  - ![img_12.png](image/img_12.png)
- TCP Reno
  - Different implementations of TCP use variations to control congestion and maximize bandwidth usage
  - E.g. TCP Reno uses two types of loss events as a signal of congestion
    - The first is the triple duplicate ACKs, which is considered mild congestion.  In this case, the congestion window is reduced to half the original.
    - The second kind of congestion detection is timeout, i.e., when no ACK is received within a specified amount of time. It is considered a more severe form of congestion, and the congestion window is reset to the initial window size.
  - ![img_13.png](image/img_13.png)
  - Lastly, we note that "probing" refers to the fact that a TCP sender increases its transmission rate to probe for the rate at which congestion begins, then backs off from that rate, and then begins probing again to see if the congestion level has changed.

---

## Slow start in TCP
- When we have a new connection that starts from a cold start, the sending host can take much longer to increase the congestion window by using AIMD. So for a new connection, we need a mechanism that can rapidly increase the congestion window from a cold start.
- To handle this, TCP Reno has a slow start phase where the congestion window is increased exponentially instead of linearly, as in the case of AIMD.
  - The source host starts by setting `cwnd` to 1 packet. When it receives the ACK for this packet, it adds 1 to the current `cwnd` and sends 2 packets. 
  - When it receives the ACK for these two packets, it adds 1 to `cwnd` for each ACK it receives. So it now sends 4 packets.
  - Once the congestion window becomes more than a threshold, often called the slow start threshold, it starts using AIMD.
![img_14.png](image/img_14.png)
![img_15.png](image/img_15.png)
- Slow start is called “slow” start despite using an exponential increase because, in the beginning, it sends only one packet and starts doubling it after each RTT. Thus, it is slower than starting with a large window.
- Finally, we note that there is one more scenario where slow start kicks in: 
  - when a connection dies while waiting for a timeout to occur. This happens when the source has sent enough data as allowed by the flow control mechanism of TCP but times out while waiting for the ACK. 
  - Thus, the source will eventually receive a cumulative ACK to reopen the connection. Then, instead of sending the available window size worth of packets at once, it will use the slow start mechanism.
- In this case, the source will have a fair idea about the congestion window from the last time it had a packet loss.
  - It will now use this information as the “target” value to avoid packet loss in the future. This target value is stored in a temporary variable, `CongestionThreshold`.
  - Now, the source performs slow start by doubling the number of packets after each `RTT` until the value of `cwnd` reaches the **congestion threshold (a knee point)**.
  - After this point, **it increases the window by 1** (additive increase) each `RTT` until it experiences packet loss (cliff point). After which, it multiplicatively decreases the window.

  
---

## TCP Fairness
- fairness means that for k connections passing through one common link with capacity R bps, each connection gets an average throughput of R/k.
- Consider a simple scenario where two TCP connections share a single link with bandwidth R. For simplicity, assume that both connections have the same RTT and only TCP segments pass through the link. Suppose we plot a graph for the throughput of these two connections. In that case, the throughput for each should sum up to R. The goal is to get the throughput achieved for each link to fall somewhere near the intersection of the equal bandwidth share line and the full bandwidth utilization line, as shown in the graph below:
![img_16.png](image/img_16.png)
- At point A in the above graph, the total utilized bandwidth is less than capacity R, so no loss can occur at this point. Therefore, both the connection will increase their window size. Thus, the utilized bandwidth's sum will grow, and the graph will move towards B.
- At point B, as the total transmission rate is more than capacity R, both connections may start having packet loss. As a result, they will decrease their window size to half and move towards point C.
- At point C, the total throughput is again less than R, so both connections will increase their window size to move towards point D and will experience packet loss at D, and so on.
- Thus, **using AIMD leads to fairness in bandwidth sharing**.

---

## Caution About Fairness
- There can be cases when TCP is not fair.
- Cases:
  - One such case arises due to the difference in the RTT of different TCP connections.
    - Recall that TCP Reno uses ACK-based adaptation of the congestion window. Thus, connections with smaller RTT values would increase their congestion window faster than those with longer RTT values. This leads to an unequal sharing of the bandwidth.
  - if a single application uses multiple parallel TCP connections.
    - nine applications using one TCP connection sharing a link of rate R. If a new application establishes a connection on the same link and also uses one TCP connection, then each application gets assigned the same transmission rate of R / 10. But, if the new application had 11 parallel TCP connections, it would get an unfair allocation of more than R / 2.

---

## Congestion Control in Modern Network Environments: TCP CUBIC
- We can see that TCP Reno has low network utilization, especially when the network bandwidth is high or the delay is large. Such networks are also known as high bandwidth delay product networks.
- To make TCP more efficient under such networks, many improvements to TCP congestion control have been proposed. Now we will look at one such version, called `TCP CUBIC`, which was also implemented in the Linux kernel. It uses a CUBIC polynomial as the growth function.
![img_17.png](image/img_17.png)
- Steps
  - Let us see what happens when TCP experiences a triple duplicate ACK, say at window=Wmax. This could be because of congestion in the network. To maintain TCP-fairness, it uses a multiplicative decrease and reduces the window to half. Let us call this Wmin.
  - Now, we know that the optimal window size would be in between Wmin and Wmax  and closer to Wmax.
  - So, instead of increasing the window size by 1, it is okay to increase the window size aggressively in the beginning.
  - Once the W approaches closer to Wmax, it is wise to increase it slowly because that is where we detected a packet loss last time. Assuming no loss is detected this time around Wmax, we keep on increasing the window a little bit
  - If there is no loss still, it could be that the previous loss was due to a transient congestion or non-congestion related event. Therefore, it is okay to increase the window size with higher values now.
- This window growth idea is approximated in TCP CUBIC using a cubic function. Here is the exact function it uses for the window growth:
  - `W(t) = C * (t - K)^3 + Wmax`
  - C = scaling constant
  - t = time since the last congestion event (packet loss)
  - K = time period that the above function takes to increase W to Wmax when there is no further loss
  - K = cube root of (Wmax * beta / C)
  - beta = multiplicative decrease factor after loss
- It is important to note that time here is the time elapsed since the last loss event instead of the usual ACK-based timer used in TCP Reno. This also makes TCP CUBIC RTT-fair.

---

## The TCP Protocol: TCP Throughput
- Given this behavior, we want to have a simple model that predicts the throughput for a TCP connection.
- To make our model more realistic, let's also assume that we have p = the probability loss. So, we assume that the network delivers 1/p consecutive packets, followed by a single packet loss.
![img_18.png](image/img_18.png)
![img_19.png](image/img_19.png)


---

## Optional Reading: Datacenter TCP
- At this point, it is essential to know that a lot of research has been going into optimizing the congestion control mechanisms. These optimizations are called for because of the evolution of the networks. We looked at TCP CUBIC as one such example for high bandwidth-delay product networks.
- Similarly, data center (DC) networks are other networks where new TCP congestion control algorithms have been proposed and implemented. There are mainly two differences that have led to this:
  - The flow characteristics of DC networks are different from the public Internet. 
    - For example, there are many short flows that are sensitive to delay. Thus, the congestion control mechanisms are optimized for delay and throughput, not just the latter alone.
  - A private entity often owns DC networks. 
    - This makes changing the transport layer easier since the new algorithms do not need to coexist with the older ones.
- DCTCP and TIMELY are two popular examples of TCP designed for DC environments. DCTCP is based on a hybrid approach of using both implicit feedback, e.g., packet loss, and explicit feedback from the network using ECN for congestion control. TIMELY uses the gradient of RTT to adjust its window.

---

## Key words
- **Segment**: The transport layer on the sending host receives a message from the application layer and appends its own header to create a segment
- **De-multiplexing**: The process of delivering the data to the correct application on the receiving host. The transport layer on the receiving host uses the port number in the segment header to determine which application to deliver the data to.


---

## Quiz
- Q1: As we have seen, UDP and TCP use port numbers to identify the sending application and destination application. Why don’t UDP and TCP just use process IDs rather than define port numbers?
  - A1: Process IDs are specific to operating systems and therefore using process IDs rather than a specially defined port would make the protocol operating system dependent. Also, a single process can set up multiple channels of communications and so using the process ID as the destination identifier wouldn’t be able to properly demultiplex, Finally, having processes listen on well-known ports (like 80 for http) is an important convention. 
- Q2: UDP and TCP use 1’s complement for their checksums. But why is it that UDP takes the 1’s complement of the sum – why not just use the sum? Exploring this further, using 1’s complement, how does the receiver compute and detect errors? Using 1’s complement, is it possible that a 1-bit error will go undetected? What about a 2-bit error?
  - A2: To detect errors, the receiver adds the four words (the three original words and the checksum). If the sum contains a zero, the receiver knows there has been an error. While all one-bit errors will be detected, but two-bit errors can be undetected (e.g., if the last digit of the first word is converted to a 0 and the last digit of the second word is converted to a 1).
- Q3: TCP utilizes the Additive Increase Multiplicative Decrease (AIMD) policy for fairness. Other possible policies for fairness in congestion control would be Additive Increase Additive Decrease (AIAD), Multiplicative Increase Additive Decrease (MIAD), and Multiplicative Increase Multiplicative Decrease (MIMD). Would these other policies converge? If so, how would their convergence behavior differ from AIMD?
  - In AIAD and MIMD, the plotted throughput line will oscillate over the full bandwidth utilization line but will not converge as was shown for AIMD. On the other hand, MIAD will converge.
  - None of the alternative policies are as stable. The decrease policy in AIAD and MIAD is not as aggressive as AIMD, so those will not effectively address congestion control. In contrast, the increase policy in MIAD and MIMD is too aggressive.
- Q4: Explain how in TCP Cubic the congestion window growth becomes independent of RTTs.
    - The key feature of CUBIC is that its window growth depends only on the time between two consecutive congestion events. One congestion event is the time when TCP undergoes fast recovery. This feature allows CUBIC flows competing in the same bottleneck to have approxi- mately the same window size independent of their RTTs, achieving good RTT-fairness.







