# Probability

## Readings
week 6:
- Chapter 12: AIMA AIMA
- R&N slides on Probability (https://gatech.instructure.com/courses/478222/files/63899987/download)

## Bayes Network
- The bayes network is a compact representation of a distribution over this very large joint probabilty distribution of all of these variables
- 

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


## Weather

## Cancer

## 

## 

## 

## 

## 

## 

## 

## 

## 

## 

## 