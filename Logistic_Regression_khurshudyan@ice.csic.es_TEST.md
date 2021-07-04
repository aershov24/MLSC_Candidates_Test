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


## **Q: Which of the following evaluation metrics can not be applied in case of logistic regression output to compare with target?**

## 1. AUC-ROC
## 1. Accuracy
## 1. Logloss
## 1. Mean-Squared-Error

**Difficulty:** Medium

**Source:**

[https://www.analyticsvidhya.com/blog/2017/08/skilltest-logistic-regression/](https://www.analyticsvidhya.com/blog/2017/08/skilltest-logistic-regression/)

**Answer:**

Solution: D

Since, Logistic Regression is a classification algorithm so it’s output can not be real time value so mean squared error can not use for evaluating it


## **Q: Why sigmoid function?**

**Difficulty:** Senior

**Source:**

[https://www.quora.com/Logistic-Regression-Why-sigmoid-function](https://www.quora.com/Logistic-Regression-Why-sigmoid-function)

**Answer:**

One of the nice properties of logistic regression is that the sigmoid function outputs the conditional probabilities of the prediction, the class probabilities. How does it work? Let's start with the so-called "odds ratio" $\frac{p}{1 - p}$, which describes the ratio between the probability that a certain, positive, event occurs and the probability that it doesn't occur - where positive refers to the "event that we want to predict", i.e., $p(y=1|x)$.
