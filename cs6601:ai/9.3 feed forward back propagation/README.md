# Feed forward Neural Networks

## Neural networks
- Neural Networks are all around us
  - Netflix recommendations
  - Online translation services
  - iPhone Virtual Assistant

## Neural network building blocks
![img.png](img/img.png)

## Single Layer Linear Model
![img_1.png](img/img_1.png)


- Loss Function
![img_2.png](img/img_2.png)

![img_3.png](img/img_3.png)

![img_4.png](img/img_4.png)
- Our loss term, is how far are we from the target value
- if spot on, it will be zero

## Combining many units
![img_5.png](img/img_5.png)
- If we combine multiple units, and sum them, we can only represent in linear 

![img_6.png](img/img_6.png)

![img_7.png](img/img_7.png)

![img_8.png](img/img_8.png)
- Activation functions within neural networks
- ReLU: a line of slope 1 up to 0, and flat after that, most commonly used

![img_9.png](img/img_9.png)

- Full diagram when we sum and combine multiple layers
![img_10.png](img/img_10.png)

## Backpropagation
- How to tweak and learn, given a model of multiple layers
![img_11.png](img/img_11.png)
- How to tweak w such that the loss or distance is minimized
![img_12.png](img/img_12.png)
- Find the direction, by which to tweak w, so that we approach w*

![img_13.png](img/img_13.png)
- Same idea can be implemented for multiple weights
![img_14.png](img/img_14.png)
- We can do to each weight of our model
![img_15.png](img/img_15.png)
- Chain rule to understand how weights of unit 2 affects unit 1
![img_16.png](img/img_16.png)
![img_17.png](img/img_17.png)
![img_18.png](img/img_18.png)
![img_19.png](img/img_19.png)
![img_20.png](img/img_20.png)
- If multiple input x, we take average of the gradients to get the gradients of our model
![img_21.png](img/img_21.png)
![img_22.png](img/img_22.png)
- Single linear example:
![img_23.png](img/img_23.png)
- We then able to tweak weights of our model, so some node weights gonna get larger, some smaller
![img_24.png](img/img_24.png)

## Neural network in practice
- pytorch and tensorflow, these auto differentiation frameworks compute the chain rule derivates for us, to update the weights of the function call
- Can multiply multiple weights, thanks to parallelism and GPUs
- ![img_25.png](img/img_25.png)
- ![img_26.png](img/img_26.png)
- ![img_27.png](img/img_27.png)

## Computational graph 
![img_28.png](img/img_28.png)
![img_29.png](img/img_29.png)
![img_30.png](img/img_30.png)
![img_31.png](img/img_31.png)
![img_32.png](img/img_32.png)
g: nonlinear activation function
b: bias term

![img_33.png](img/img_33.png)
![img_34.png](img/img_34.png)
![img_35.png](img/img_35.png)
![img_36.png](img/img_36.png)
![img_37.png](img/img_37.png)
- Use of chain rule

## Back propagation
![img_38.png](img/img_38.png)
![img_39.png](img/img_39.png)
![img_40.png](img/img_40.png)
![img_41.png](img/img_41.png)
![img_42.png](img/img_42.png)
![img_43.png](img/img_43.png)
![img_44.png](img/img_44.png)
![img_45.png](img/img_45.png)
![img_46.png](img/img_46.png)
![img_47.png](img/img_47.png)
![img_48.png](img/img_48.png)



## 

## 

## 