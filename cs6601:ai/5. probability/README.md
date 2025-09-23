# Probability

## Readings
week 6:
- Chapter 12: AIMA AIMA
- R&N slides on Probability (https://gatech.instructure.com/courses/478222/files/63899987/download)

## Bayes Network
- The bayes network is a compact representation of a distribution over this very large joint probabilty distribution of all of these variables

## Coin Flip
- What is the probability of flipping a coin where p(x1=x2=x3=x4)? 
- p(H) = p(T) = 0.5
- p(H,H,H,H) = P(T,T,T,T) = 0.0625
- p(x1=x2=x3=x4) = p(H,H,H,H) + P(T,T,T,T) = 0.0625 + 0.0625 = 0.125


- What is the probability of flipping a coin where p(x1,x2,x3,x4) >= 3H?
- p(H) = p(T) = 0.5
- p(x1=x2=x3=x4) = 0.125
- H H H H
- H H H T
- H H T H
- H T H H
- T H H H
- 5 * 1/16
- 0.3125

## Probabilty
- Complementary probability
  - P(A) = p => P(!A) = 1 - p
- Independence
  - X ind Y : P(X)P(Y) = P(X,Y)

## Dependence
- What is probability of P(X2=h), given that
- P(X1 = H)=0.5 
- P(X2=H | X1 =H)=0.9 
- P(X2=T | X1 =T)=0.8
- We can use theorm of prob
- P(X2=H) = P(X2=H | X1=H) * P(X1=H) + P(X2=H | X1=T) * P(X1=T)
- P(X2=H) = 0.9  * 0.5 + 0.2 * 0.5
- P(X2=H) = 0.55

## Total Probability
- P(Y) = Sum of (P(Y | Xi))P(Xi)
- P(!X|Y) = 1 - P(X|Y)

## Weather
- P(D1=sunny) = 0.9
- P(D2=sunny | D1=sunny) = 0.8
- P(D2=rainy | D1=sunny) = ? 
- 0.2


- P(D1=sunny) = 0.9
- P(D2=sunny | D1=sunny) = 0.8
- P(D2=rainy | D1=sunny) = 0.2
- P(D2=sunny | D1=rainy) = 0.6
- P(D2=rainy | D1=rainy) = ?
- 1 - 0.6 = 0.4


- P(D2=sunny) = ?
- P(D2=sunny | D1=sunny) * P(D1=sunny) + P(D2=sunny | D1=rainy) * P(D1=rainy) = 0.9 * 0.8 + 0.6 * 0.1 = 0.78
- P(D3=sunny) = ?
- 0.78 * 0.8 + 0.22 * 0.6 = 0.624 + 0.132 =0.756

## Cancer
- P(C) = 0.01
- P(¬C) = 0.99
- P(+ | C) = 0.9
- P(- |C) = ?
- 0.1

Joint probability
- P(C) = 0.01
- P(¬C) = 0.99
- P(+ | C) = 0.9
- P( - |C) = 0.1
- P(+| ¬C) = 0.2
- P(-| ¬C) = 0.8


- P( + , C) = ?
- P( + , C)  = 0.9 * 0.01 = 0.009
- P( - , C) = ? 
- P( - , C) = 0.1 * 0.01 = 0.001
- P( + , ¬C) = ?
- P( + , ¬C) = 0.1 * 0.01 = 0.198
- P( - , ¬C) = ?
- P( - , ¬C) = 0.8 * 0.99 = 0.792
- P( C | +) = ?
- 0.009 / (0.009 + 0.198)
- 0.043

## Bayes Rule 
- P(A|B) = P(B|A) * P(A) / P(B)
- Posterior = Likelihood * Prior / Marginal Likelihood
- P(B) = sum of P(B|Ai) * P(Ai) = total probability

- P ( C | +) = P( + | C) * P(C) / P(+)
- P ( C | +) = 0.9 * 0.01 / (0.9 * 0.01 + 0.2 * 0.99) = 0.043
