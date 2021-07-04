## **Topic: Logistic Regression**

**Author:** Martiros Khurshudyan

**QAs Total:** 3

## **Q: What is decision boundary in Logistic Regression?**

**Difficulty:** Junior

**Source:**

[https://towardsdatascience.com/logistic-regression-detailed-overview-46c4da4303bc](https://towardsdatascience.com/logistic-regression-detailed-overview-46c4da4303bc)

**Answer:**


To predict which class a data belongs, a threshold can be set. Based upon this threshold, the obtained estimated probability is classified into classes.
Say, if predicted_value > 0.5, then classify email as spam else as not spam.
Decision boundary can be linear or non-linear. Polynomial order can be increased to get complex decision boundary.


## **Q: Why can’t linear regression be used in place of logistic regression for binary classification?**

**Difficulty:** Medium

**Source:**

[https://www.upgrad.com/blog/machine-learning-interview-questions-answers-logistic-regression/](https://www.upgrad.com/blog/machine-learning-interview-questions-answers-logistic-regression/)


**Answer:**

The reasons why linear regressions cannot be used in case of binary classification are as follows:

1. Distribution of error terms: The distribution of data in case of linear and logistic regression is different. Linear regression assumes that error terms are normally distributed. In case of binary classification, this assumption does not hold true. 

1. Model output: In linear regression, the output is continuous. In case of binary classification, an output of a continuous value does not make sense. For binary classification problems, linear regression may predict values that can go beyond 0 and 1. If we want the output in the form of probabilities, which can be mapped to two different classes, then its range should be restricted to 0 and 1. As the logistic regression model can output probabilities with logistic/sigmoid function, it is preferred over linear regression.

1. Variance of Residual errors: Linear regression assumes that the variance of random errors is constant. This assumption is also violated in case of logistic regression.


## **Q: Why sigmoid function?**

**Difficulty:** Senior

**Source:**

[https://www.quora.com/Logistic-Regression-Why-sigmoid-function](https://www.quora.com/Logistic-Regression-Why-sigmoid-function)

**Answer:**

One of the nice properties of logistic regression is that the sigmoid function outputs the conditional probabilities of the prediction, the class probabilities. How does it work? Let's start with the so-called "odds ratio" $\frac{p}{1 - p}$, which describes the ratio between the probability that a certain, positive, event occurs and the probability that it doesn't occur - where positive refers to the "event that we want to predict", i.e., $p(y=1|x)$.
