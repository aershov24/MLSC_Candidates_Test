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

The main goal of **Gradient descent** is to minimize the cost value. i.e. `min J(θ)`. Now to minimize our cost function we need to run the gradient descent function on each parameter i.e.

<p align="center"><img width="200" src="https://miro.medium.com/max/306/1*1--MUhjPjOL7oYdVo7R6gQ.png")</p>

<h5 align="center">To minimize the cost function we have to run the gradient descent function on each parameter</h5>

<p align="center"><img width="600" src="https://miro.medium.com/max/875/1*Ecea3jVIRxK4Mkrh_Nie4w.jpeg")</p>

<h5 align="center">Gradient Descent Simplified | Image: Andrew Ng Course</h5>

**Gradient descent** has an analogy in which we have to imagine ourselves at the top of a mountain valley and left stranded and blindfolded, our objective is to reach the bottom of the hill. Feeling the slope of the terrain around you is what everyone would do. Well, this action is analogous to calculating the gradient descent, and taking a step is analogous to one iteration of the update to the parameters.

![](https://miro.medium.com/max/875/1*SzVGKaga11mEwpJ1EpQJOw.png)

---
## Q: Why to use Stochastic Gradient Descent in Logistic Regression model?

**Difficulty:** `Senior`

**Source:** 

[https://machinelearningmastery.com/logistic-regression-tutorial-for-machine-learning/](https://machinelearningmastery.com/logistic-regression-tutorial-for-machine-learning/).

**Answer:** 

**Stochastic gradient descent** is used to solve the problem of finding the coefficients for the logistic regression model. There are two ways to find it:

  * Calculate a prediction using the current values of the coefficients.
  * Calculate new coefficient values based on the error in the prediction.

The process is repeated until the model is accurate enough (e.g. error drops to some desirable level) or for a fixed number iterations. You continue to update the model for training instances and correcting errors until the model is accurate enough orc cannot be made any more accurate. It is often a good idea to randomize the order of the training instances shown to the model to mix up the corrections made.

By updating the model for each training pattern we call this online learning. It is also possible to collect up all of the changes to the model over all training instances and make one large update. This variation is called batch learning and might make a nice extension to this tutorial if you’re feeling adventurous.

* **Calculate Prediction**

Let’s start off by assigning `0.0` to each coefficient and calculating the probability of the first training instance that belongs to `class 0`.

B0 = 0.0

B1 = 0.0

B2 = 0.0

The first training instance is: x1=2.7810836, x2=2.550537003, Y=0

Using the above equation we can plug in all of these numbers and calculate a prediction:

prediction = 1 / (1 + e^(-(b0 + b1*x1 + b2*x2)))

prediction = 1 / (1 + e^(-(0.0 + 0.0*2.7810836 + 0.0*2.550537003)))

prediction = 0.5

* **Calculate New Coefficients**

We can calculate the new coefficient values using a simple update equation.

b = b + alpha * (y – prediction) * prediction * (1 – prediction) * x

Where `b` is the coefficient we are updating and prediction is the output of making a prediction using the model.

Alpha is parameter that you must specify at the beginning of the training run. This is the learning rate and controls how much the coefficients (and therefore the model) changes or learns each time it is updated. Larger learning rates are used in online learning (when we update the model for each training instance). Good values might be in the range `0.1` to `0.3`. Let’s use a value of `0.3`.

You will notice that the last term in the equation is `x`, this is the input value for the coefficient. You will notice that the `B0` does not have an input. This coefficient is often called the bias or the intercept and we can assume it always has an input value of `1.0`. This assumption can help when implementing the algorithm using vectors or arrays.

Let’s update the coefficients using the prediction `(0.5)` and coefficient values `(0.0)` from the previous section.

b0 = b0 + 0.3 * (0 – 0.5) * 0.5 * (1 – 0.5) * 1.0

b1 = b1 + 0.3 * (0 – 0.5) * 0.5 * (1 – 0.5) * 2.7810836

b2 = b2 + 0.3 * (0 – 0.5) * 0.5 * (1 – 0.5) * 2.550537003

or

b0 = -0.0375

b1 = -0.104290635

b2 = -0.09564513761

* **Repeat the Process**

We can repeat this process and update the model for each training instance in the dataset. A single iteration through the training dataset is called an epoch. It is common to repeat the stochastic gradient descent procedure for a fixed number of epochs.

At the end of epoch you can calculate error values for the model. Because this is a classification problem, it would be nice to get an idea of how accurate the model is at each iteration.

<p align="center"><img width="500" src="https://machinelearningmastery.com/wp-content/uploads/2016/02/Logistic-Regression-with-Gradient-Descent-Accuracy-versus-Iteration.png")</p>

<h5 align="center">Logistic Regression with Gradient Descent Accuracy versus Iteration</h5>

You can see that the model very quickly achieves 100% accuracy on the training dataset.

The coefficients calculated after 10 epochs of stochastic gradient descent are:

b0 = -0.4066054641

b1 = 0.8525733164

b2 = -1.104746259

---
