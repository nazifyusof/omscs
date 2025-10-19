# Machine Learning

## Readings
- Read AIMA: Chapter 19.1-19.5, 19.7, 20.1-20.2
- R&N slides on Learning from Observation: Decision Trees (18.1-18.3); http://www.cc.gatech.edu/~thad/6601-gradAI-fall2015/chapter18.pdf  
- R&N slides Statistical Learning (20.1-20.2) https://faculty.cc.gatech.edu/~thad/6601-gradAI-fall2015/chapter20a.pdf

- On Campus sides: https://faculty.cc.gatech.edu/~thad/6601-gradAI-fall2015/decision-trees.pdf

## K-Nearest Neighbors (KNN)
- ![img.png](img/img_1.png)
- KNN is based on the idea that similar examples should have similar classifications.
- To classify a new instance, KNN looks at the 'k' closest training examples in
- Try multiple values of k and see which one works best on a validation set.

## Cross Validation
- Often a researchers spend a lot of time to make recognizer only to find out the data does not represent the problem
- Use 80% of data for training, and 20% for testing to avoid overfitting
- With k = 1 and training and testing on same data, accuracy is 100% but it is not a good model
- Always choose randomly chosen training and testing data to avoid bias
- Shark example:
- ![img.png](img/img_2.png)


Steps:
1. We select 80%, and 20% randomly
2. For each example in the 20% independent test est, we compare it to training data
3. Sicne we use k = 3, we find 3 nearest neighbors
4. We label each test example based on majority vote of its neighbors and compare to actual label
5. Then, we calculate percentage correct and report the accuracy
6. Not done yet, we could've gotten lucky
7. Repeat the process multiple times with different random splits of training and testing data
8. 100 iterations, and average the accuracy over all iterations to get a better estimate of true accuracy


- If we dont know the value of K, we can use cross validation to find the best K
- K = 1, 100 iterations, then do the same for K = 2,3,..., do cross validations
- Then, choose the K with the highest average accuracy


Netflix prize (Million dollar prize to improve movie recommendation system):
- Use the same strategy we talk about above 
- Netflix has millions of dataset, what if we have few? Do leave-one-out cross validation
- LOOCV, Leave one out for cross-validation
- Training on 8, test on 2 leaves 10 choose 2 possibilities which is 45
- If we are using KNN, and if we see a huge difference in K = 10 and K = 11, there is a problem with data


Quiz: 
![img.png](img/img_3.png)
- Not A because we might be lucky with training and testing data

## Gaussian Distribution
- The bell curve, also known as normal distribution

## Central Limit Theorem
- Very loosely, if we have enough independent random variables, their sum tends toward a Gaussian distribution
- If we have enough factors influencing students grade, the distribution of grades will be Gaussian

## Pattern recognition with Gaussion Distribution
- ![img.png](img/img_4.png)
- ![img.png](img/img_5.png)
- ![img.png](img/img_6.png)
- ![img.png](img/img_7.png)
- Suppose I get an insect with length of 3 units, is it a grasshopper or katydid?
- Probably a grasshopper because the height of the blue curve at 3 is higher than the height of the red curve at 3
- The formula for P(X) is given by:
$$
P(X) = \frac{1}{\sigma \sqrt{2\pi}} \, e^{ -\frac{(X - \mu)^2}{2\sigma^2} }
$$
 

## Decision Boundaries
- What happen if x falls when X and Y have the same probability?
- ![img_1.png](img/img_8.png)
- Anythihng on the left is classified as katydid, anything on the right is grasshopper
- ![img.png](img/img_9.png)
- Both red and blue have the same mean, but different variances
- The one with lower SD is skinnier (red)
- On either side of the middle, the fatter one has higher probability and wins


## RECOGNITION QUIZ:
Given data consisting of 10% positive examples and 90% negative examples, should i believe that a recognizer that works 90% of the time is working?
- No, It is possible that the recognizer does really well on the negative examples, or even blindly predicts everything to be negative!
- This doesn't say anything conclusive about how it might work on the positive examples, and we can't be sure about its overall performance.


## Error
- WE can use graph to visualize error
- ![img.png](img/img_10.png)
- To the left of decision boundary, we could measure error by integrating right gausion from -ve infinity to boundary
- Let's reimagine above as graph of mosquito carrying dengue fever (red) and NOT carrying dengue fever (blue)
- We want to spray pesticide only on mosquitos carrying dengue fever
- We want to error on the side of caution, we want to minimize false negatives (blue area on right)
- We can move the decision boundary to the right, reducing errors
- But how much can we move it? WE can weight our decision based on cost of errors


## Bayes Classifier 
$$
P(C_j \mid d) = \frac{P(d \mid C_j) \cdot P(C_j)}{P(d)}
$$

# BAYES QUIZ:
- Which is more likely, Drew is a male or female? 
- ![img.png](img/img_11.png)

## Naive Bayes
- Assuming all features are independent, we can represent the problem as Bayes Nets
- The features are conditionally independent given the class
- We are assuming that each class has different distribution for the features
- Thus we can model a net such that C_j is at the top, with arrows pointing to each feature
- Because the class is the cause and feature distrbutions are the effects
- ![img_1.png](img/img_12.png)
- ![img.png](img/img_13.png)
- We can represent any Naive Bayes classifier in this sort of general framework witht he class pointing to the features


## Maximum likelihood
- Assume that all classes are equally likely, the one that maximize the equation is the one we assign the data
- Why we say all classes are equally likely? Because we dont trust and dont have any prior knowledge about the classes
- 


## NAIVE BAYES QUIZ: 
![img.png](img/img_14.png)


## No free lunch
- There is no one learning algorithm that is best for all problems
- Wolpert McReady: for any algorithm, any elevated performance over one class of problems is offset by performance of another class


## Naive Bayes VS KNN
- Shark bites problem: 
- ![img.png](img/img_1.png)
- THe border between classification depends on the noisiness of data of the shark bites

- Mixture of Gausians to tackle the issue
- ![img.png](img/img_15.png)
- Kernel Density Estimation: In between two extremes, we could use fewer Gaussians which would cause the decision boundary to be smooth, but still give good continous estimates for each class
- We could use cross Validation to find the best number of Gaussians to use
- 

## Generalization 
- We need to find a method that classifies data with the highest accuract, doesnt overfit, and generalize well with our training data to our unseen data without losing its discriminative power
- How do we choose methods in Machine Learning?

## Visualization
- One of the first things to do is to visualize the data
- if most of the classes from balls of data without many concavities, gaussian methods would work well
- if there are situations where classes interpenetrate but still have distinct boundaries, KNN or the Kernel methods would work well
- Sometimes data is high dimensional that it's hard to visualize
- For those methods, we could use decision trees and boosting methods

## Decision Trees
![img.png](img/img_16.png)
- If we have continuous value instead of discrete values, we create threshold for the attribute

## Entropy and Infomation Gain

$$
\text{Remainder}(A) = \sum_k \frac{P_k + N_k}{P + N} \cdot B\left( \frac{P_k}{P_k + N_k} \right)
$$

$$
B(q) = -q \log_2 q - (1 - q) \log_2 (1 - q)
$$

$$
\text{Information Gain}(A) = B\left( \frac{P}{P + N} \right) - \text{Remainder}(A)
$$

## ENTROPY QUIZ:
![img.png](img/img_17.png)
![img.png](img/img_18.png)
- Why?
$$
\text{Gain}(\text{outlook}) = 0.940 - \left( \frac{5}{14} B\left(\frac{2}{5}\right) + \frac{4}{14} B\left(\frac{4}{4}\right) + \frac{5}{14} B\left(\frac{3}{5}\right) \right) = 0.246
$$

- 0.940 = Total entropyy
- 5/14 = Probability of sunny
- 4/14 = Probability of overcast
- 5/14 = Probability of rainy
- B(2/5) = Entropy of sunny = 2 results in yes
- B(4/4) = Entropy of overcast = 4 results in yes
- B(3/5) = Entropy of rainy = 3 results in yes


## Random Forest 
- Bagging (Bootstrap Aggregating)
- Input: Data set of Size N with M Dimensions
  - SAMPLE n times from Data
  - SAMPLE m times from attributes
  - Learn TREE on sample DATA and ATTRIBUTES
- Repeat until k trees
- The random sampling seems to help avoid overfitting, which is often a problem in decision trees
- One nice thing about DT is that they tell you which features are teh most useful automatically
- One issue is trees might get too big, we can limit decision tree leaves, easy to examine
- Lots of trees and forest, we can see how stable the feature importance is
- 
- 

## Boosting
- Combine many weak classifiers to form an ensemble that can do the classifier task
- alpha = 0.5 * ln((1 - error) / error) > 0
- if the example is classified wrong, we multiply its weight by e^(alpha)
- If the example is classified right, we multiply its weight by - e^(alpha)
![img.png](img/img_19.png)
- Example above where we look at the top right -ve, 
  - first classifier is wrong, hence -0.42
  - second classifier is wrong, hence -0.65
  - third classifier is right, hence +0.92
  - Total is -0.15, hence classified as -ve
- The ensemble is correct! 
- We just keep monitoring the error during boosting and stop when it converges
- Like decision trees, boosting also gives feature importance

## Neural Nets
![img.png](img/img_20.png)
- Model neurons using inputs, biased weights, a non-linear function that represents the neurons body, and outputs
- Non-linear function could be;
  - Simple step function
  - Probit, which is basically the Gaussian integrated
- Depends on problem, which is better. Most people prefer smooth functions like probit


Can create logic gates with neural nets
- AND: W0 = -1.5, W1 = 1, W2 = 1
- OR: W0 = -0.5, W1 = 1, W2 = 1
- NOT: W0 = 0.5, W1 = -1
- NOR: W0 = 0.5, W1 = -1, W2 = -1


## Multiplayer Nets
- Feedforward nets: it has no internal states, implement functions based on their inputs
- 

## Perceptron Learning
![img.png](img/img_21.png)
- A single layer perceptron can only do linear decision boundaries,
- In linear boundary we can learn functions like AND and OR, but not XOR, because XOR is not linearly separable.
- For DT, it would need to make a full tree with n levels in order to do a good job, need to see 2^n unique examples to get it
- DT does much better with a lot less examples


## Multilayer Perceptrons
- Can learn nonlinear decision boundaries — e.g., can solve XOR. 
- Extension of single-layer perceptron with one or more hidden layers.


## Back Propagation
- How do we train Multilayer Perceptrons? Back propagation
- ![img.png](img/img_22.png)
- Output Layer
  - Err i ​: difference between target and actual output
  - g ′(in_i ​): derivative of activation function at neuron 𝑖
- Hidden Layer
  - Error is back-propagated from output layer to hidden layer
  - Weighted sum of downstream deltas scaled by local derivative.
  - This connects the output layer’s errors back to hidden layer neurons.
- Weight Update for Hidden Layer
  - a_k: activation from previous layer (input to hidden)
  - delta_j: propagated error for hidden node
- Notes:
  - alpha: learning rate
  - g'(in): derivative of activation 
  - Back propagation applies chain rule to distribute output error backward through layers
  - Each layer adjusts weights to minimize total network error
  - In neural nets, the process of updating the weights and then summing teh gradient updates for the training examples are called **EPOCH**
  - ML researchers can tell how hard a problem is by how long it takes to converge
![img.png](img/img_23.png)
![img_1.png](img/img_24.png)
  - DT converges faster, but multilayer network eventually gets there

## Deep Learning
- Use hiererical structures to solve problems
- In DT, human can understand how a decision is made by traversing the tree
- With NN, it gets more complex on determining what the system is doing
- It might be hard to use the system to understand of the problem domain, BUT many problems only care more about the performance


## Unsupervised Learning
- Algorithm is given a set of data without labels, and it attempts to determine what classes are in the data, and which data belongs to which class
- Useful when we have lots of data that's hard to label
- K-means below:

## k-Means and EM
- With K means, we specify the number of classes in a dataset

| 1                             | 2                          | 3                          | 4                   | 
|:------------------------------|:---------------------------|:---------------------------|---------------------|
| ![img_25.png](img/img_25.png) | ![img.png](img/img_26.png) | ![img.png](img/img_27.png) | ![img.png](img/img_28.png) |

- Start by putting 2 means randomly in the data
- EXPECTATION: Take every point in db and assign it to the nearest mean
- MAXIMIZATION: We recalculate the mean based on the assignment of the points to each of the clusters
- Repeat expectation step, re-estimate the mean again, use the new mean to create new decision boundary to reclassify the data
- Repeat until the means and the assignments of the points to the clusters dont change
![img.png](img/img_29.png)
- What if we get stuck and doesnt converge? 
  - We can try random restart like we did with hill climbing in Simulated Annealing

## EM and Mixture of Gaussian
- We can fit mixture of Gaussians to the data
- We can use the same EM approach to find each Gaussian's Variance and Mean
- Before we do EM, we need to know how many Gaussians to use

| L = 0                         | 1                          | 2                          | 5                          | 20 |
|:------------------------------|:---------------------------|:---------------------------|----------------------------|----|
| ![img.png](img/img_30.png) | ![img.png](img/img_26.png) | ![img.png](img/img_32.png) | ![img.png](img/img_33.png) | ![img.png](img_34.png)   |

- Because we had more params to estimate, it took 20 EM for Gaussian, and 4 for K-Means
- Increasing the dimensions to estimate always requires more time and data to complete
- 