# Stochastic Approximations

## Introduction
![img.png](img/img.png)

- Batch gradient
  - Uses full training to set to compute delta L (Often Hessian)
- Online(stochastic) gradient
  - Pick a single random sample, compute a(noisy) update step
  - Often done with mini-batch of samples (smaller than full dataset)
  - Better use of parallet compute (GPU or distributed)
- Both udpate rules can be written
  - Batch:  θ_j+1 ← θ_j − α * psi * ∇L(θ_j), for a scaling matrix psi

Typically
- Batch methods:
  - Converge more quickly (fewer iterations)
  - Have more expensive updates
- Online methods:
  - Converge slowly, especially near optimum, due to noise
  - Have less expensive update rules

![img_1.png](img/img_1.png)

![img_2.png](img/img_2.png)

![img_3.png](img/img_3.png)

![img_4.png](img/img_4.png)

- If we produce K sets of samples, then we get K variants of empirical loss
- Each time we are going to get slightly different example
- What we do with K fold cross validation is to use what we have in K, hopefully not totally correlated ways, and average over those
- If we had access to all the data in the world, we could take as much as we want and train as much as we want, we'll be able to get as close as possible to true loss
- But it;s not practical since we have limited data
- Compute what we can with what we have

![img_5.png](img/img_5.png)

![img_6.png](img/img_6.png)

## Stochastic Approximation Algorithms
![img_7.png](img/img_7.png)
- A is black, B i is blue
- Find a zero of the gradient.
  - A is the gradient of the expected loss
  - B is the gradient of the empirical loss, B is gradient of L_n

![img_8.png](img/img_8.png)

![img_9.png](img/img_9.png)

![img_10.png](img/img_10.png)

![img_11.png](img/img_11.png)

![img_12.png](img/img_12.png)

![img_13.png](img/img_13.png)

![img_14.png](img/img_14.png)

## Rates of Convergence
![img_15.png](img/img_15.png)

![img_16.png](img/img_16.png)

![img_17.png](img/img_17.png)

![img_18.png](img/img_18.png)

## Convex Functions
![img_19.png](img/img_19.png)

![img_20.png](img/img_20.png)

![img_21.png](img/img_21.png)

![img_22.png](img/img_22.png)
## Convergence of Robbins-Monro
![img_23.png](img/img_23.png)

- WHy robbins-monroe? 
  - WE know they are very fast for optimization
  - Newton's method also converges quadratically
- Is SGD used just for practical resons? or ist theres something deep?
![img_24.png](img/img_24.png)

![img_25.png](img/img_25.png)

![img_26.png](img/img_26.png)

![img_27.png](img/img_27.png)

![img_28.png](img/img_28.png)

![img_29.png](img/img_29.png)

![img_30.png](img/img_30.png)

## Summary - Robbins-Monro

- In more recent years, data is essentially infinite
- With billions of data points, we're quite close to L_infinity
- Don't need to resuse data, visit each data point once only

- In the Big Data setting, we can aim for L_infinity
  - Don't just consider number of model update steps
  - The amount of data we make use of is the key factor in bounding our performance

- What if we don;t have infinite data?
  - We may chose to add regulariation to prevent overfitting
  - Weight decay, dropout, and etc

- However, data augmentation is a very effective regularizer
  - Good augmentation can effectively make the dataset infinite, which brings the objective close to L_infinity


- In this Robbins-Monro sense, it is arguably the ideal regularizer


IN SUMMARY
- Converging to L_N and L_infinity are very different
- No method can beat Cramer-Rao as data grows
- The best method makes good use of the most data in the least time

Further
- SGD and online methods have practical advantages
- Moderate memory requirements, lower compute means visiting more data points, noise acts like annealing, etc
