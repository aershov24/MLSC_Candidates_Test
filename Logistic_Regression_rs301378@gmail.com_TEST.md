# Topic: Logistic regression
**Author**: Rohit Sharma

**QAs Total:** 3

---

## Q: Why is logistic regression called regression and not classification?

**Difficulty:** `Junior`

**Source:**

[https://medium.com/analytics-vidhya/interview-questions-on-logistic-regression-1ebd1666bbbd](https://medium.com/analytics-vidhya/interview-questions-on-logistic-regression-1ebd1666bbbd)

**Answer:**

The main difference between **regression** and **classification** is that the output variable in regression is numerical (or continuous) while that for classification is categorical (or discrete).Logistic regression is basically a supervised classification algorithm. However, the model builds a regression model just like linear regression to predict the probability that a given data entry belongs to the category numbered as “1”.
For example, with binary classification, let ‘x’ be some feature and ‘y’ be the output which can be either `0` or `1`.
The probability that the output is `1` given its input can be represented as:

$$p(y=1|x)$$

If we predict the probability via linear regression, we can state it as:

$$p(X) = β0 + β1X$$

where, `p(x) = p(y=1|x)`
Logistic regression model can generate the predicted probability as any number ranging from negative to positive infinity, whereas probability of an outcome can only lie between `0< P(x)<1`. However, to mitigate the problem of outliers a sigmoid function is used in logistic regression. The linear equation is put in the sigmoid function.

$$g(x) = \frac{1}{1+e^{\smash{-x}}\right}$$

---

## Q: Is it possible to use Coast function in logistic regression? How it is different from Gradient Decent?

**Difficulty:** `Medium`

**Source:** 

[https://towardsdatascience.com/introduction-to-logistic-regression-66248243c148](https://towardsdatascience.com/introduction-to-logistic-regression-66248243c148)

**Answer:**
No, we cannot use Coast function `J(0)` in logistic regression. It end up being a non-convex function with many local minimums, in which it would be very difficult to minimize the cost value and find the global minimum. 

![](https://miro.medium.com/max/3000/1*dPXwswig8RTCAjstnUZNGQ.png)

For logistic regression, the Cost function is defined as:

$$−log(hθ(x)) if y = 1$$
$$−log(1−hθ(x)) if y = 0$$

Coast(h_{0}(x),y) = log \begin{cases}
                        −log(hθ(x))  &\text{if } y = 1 \\
                        −log(1−hθ(x)) &\text{if } y = 0
                        \end{cases}

In case `y=1`, the output (i.e. the cost to pay) approaches to `0` as `hθ(x)` approaches to `1`. Conversely, the cost to pay grows to infinity as `hθ(x)` approaches to `0`. You can clearly see it in the plot below, left side. This is a desirable property: we want a bigger penalty as the algorithm predicts something far away from the actual value. If the label is `y=1` but the algorithm predicts `hθ(x)=0`, the outcome is completely wrong.

Conversely, the same intuition applies when `y=0`, depicted in the plot below, right side. Bigger penalties when the label is `y=0` but the algorithm predicts `hθ(x)=1`.

![](https://miro.medium.com/max/875/1*ejwj2sFEgSA5yisYvbtSKQ.png)

The above two functions can be compressed into a single function i.e.

![](https://miro.medium.com/max/1400/1*_52kKSp8zWgVTNtnE2eYrg.png)

The main goal of Gradient descent is to minimize the cost value. i.e. `min J(θ)`. Now to minimize our cost function we need to run the gradient descent function on each parameter i.e.

<p align="center"><img width="200" src="https://miro.medium.com/max/306/1*1--MUhjPjOL7oYdVo7R6gQ.png")</p>

<h5 align="center">To minimize the cost function we have to run the gradient descent function on each parameter</h5>

<p align="center"><img width="600" src="https://miro.medium.com/max/875/1*Ecea3jVIRxK4Mkrh_Nie4w.jpeg")</p>

<h5 align="center">Gradient Descent Simplified | Image: Andrew Ng Course</h5>

Gradient descent has an analogy in which we have to imagine ourselves at the top of a mountain valley and left stranded and blindfolded, our objective is to reach the bottom of the hill. Feeling the slope of the terrain around you is what everyone would do. Well, this action is analogous to calculating the gradient descent, and taking a step is analogous to one iteration of the update to the parameters.

![](https://miro.medium.com/max/875/1*SzVGKaga11mEwpJ1EpQJOw.png)

---
## Q: Provide a mathematical intuition of Logistic Regression

**Difficulty:** `Senior`

**Source:** 

[https://medium.com/@nikethnarasimhan/logistic-regression-an-intuitive-approach-b1ece5b13c#:~:text=Logistic regression is a statistical,many more complex extensions exist](https://medium.com/@nikethnarasimhan/logistic-regression-an-intuitive-approach-b1ece5b13c#:~:text=Logistic%20regression%20is%20a%20statistical,many%20more%20complex%20extensions%20exist).

**Answer:** 

Logistic regression can bee seen as a **transformation** from linear regression to logistic regression using the logistic function, also known as the **sigmoid function** or S(x):

$$S(x) = \frac{1}{1+e^{-x}}$$

Given the linear model: 

$$y = b_0 + b_1 \cdot x$$

If we apply the sigmoid function to the above equation it results: 

$$S(y) = \frac{1}{1+e^{-y}} = p$$

where `p` is the probability and it takes values between 0 and 1. If we now apply the logit function to `p`, it results: 

$$logit(p) = log(\frac{p}{1-p}) = b_0 + b_1 \cdot x$$

The equation above represents the logistic regression. It fits a logistic curve to set of data where the dependent variable can only take the values 0 and 1. 

The previous transformation can be illustrated in the following figure:
![](https://miro.medium.com/max/3000/1*dPXwswig8RTCAjstnUZNGQ.png)

