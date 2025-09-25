# Probability

## Readings
week 6:
- Chapter 12: AIMA AIMA
- R&N slides on Probability (https://gatech.instructure.com/courses/478222/files/63899987/download)

## Bayes Network
- A (not observable) -> B (observable)
- P(A) -> P(B|A) P(B|!A)
- How many parameters do we need to specify this distribution?
- P(A) = 1 parameter
- P(B|A) = 1 parameter
- P(B|!A) = 1 parameter
- Total = 3 parameters

## Computing Bayes Rule
- $P(A \mid B) = \frac{P(B \mid A) \cdot P(A)}{P(B)}$
- $P(!A \mid B) = \frac{P(B \mid !A) \cdot P(!A)}{P(B)}$


- $P(A \mid B) + P(!A \mid B) = 1$


- $P'(A \mid B) = P(B \mid A) \cdot P(A)$
- $P'(!A \mid B) = P(B \mid !A) \cdot P(!A)$

- $P(A \mid B) = \eta(normalizer) \cdot P'(A \mid B)$
- $P(!A \mid B) = \eta(normalizer) \cdot P'(!A \mid B)$
- $\eta = \frac{1}{P'(A \mid B) + P'(!A \mid B)}$


##  Two Test Cancer Example 1
- P(C) = 0.01
- P(+|C) = 0.9
- P(-|!C) = 0.8


- P(!C) = 0.99
- P(-|C) = 0.1
- P(+|!C) = 0.2


- P(C|T1=+, T2=+) = P(C|++) = ?

| | prior | + | + | P' |
|------|-------|------|------|------|
| C | 0.01 | 0.9 | 0.9 | 0.0081 |
| !C | 0.99 | 0.2 | 0.2 | 0.0396 |

- P(C|++) = 0.0081 / (0.0081 + 0.0396) = 0.1698
- P(!C|++) = 0.0396 / (0.0081 + 0.0396) = 0.8302


##  Two Test Cancer Example 2

- P(C) = 0.01
- P(+|C) = 0.9
- P(-|!C) = 0.8


- P(!C) = 0.99
- P(-|C) = 0.1
- P(+|!C) = 0.2


- P(C|T1=+, T2=-) = P(C|+-) = ?

| | prior | + | -   | P'     |
|------|-------|------|-----|--------|
| C | 0.01 | 0.9 | 0.1 | 0.0009 |
| !C | 0.99 | 0.2 | 0.8 | 0.1584 |

- P(C|+-) = 0.0009 / (0.0009 + 0.1584) = 0.00568181818
- P(!C|+-) = 0.1584 / (0.0009 + 0.1584) = 0.99431818181

##  Conditional Independence
- P(T2|C,T1) = P(T2|C)
- Given C, T1 does not provide any additional information about T2
- Consider the graph 
- C -> T1, C -> T2
- If we know C, T1 and T2 are independent


- Given graph A -> B, A -> C
- Given A, B and C are independent
- Is (B ind C | A) == B ind C? **No**


- P(C) = 0.01
- P(+|C) = 0.9
- P(-|!C) = 0.8
- What is P(T2+|T1+) = P(+|+) = ?
- ![img_1.png](img/img_1.png)


- A⊥B⇒A⊥B∣C? False
- A⊥B∣C⇒A⊥B? False


![img.png](img/img_2.png)
- 0.01 because R and S are independent


##  

##  

##  

##  

##  

##  

##  

##  

## 