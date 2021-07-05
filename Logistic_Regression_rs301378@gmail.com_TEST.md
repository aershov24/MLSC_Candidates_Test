# Topic: Logistic regression


## Q: Why is logistic regression called regression and not classification?

**Difficulty:** `Junior`

**Source:**

[https://medium.com/analytics-vidhya/interview-questions-on-logistic-regression-1ebd1666bbbd](https://medium.com/analytics-vidhya/interview-questions-on-logistic-regression-1ebd1666bbbd)

**Answer:**

The main difference between regression and classification is that the output variable in regression is numerical (or continuous) while that for classification is categorical (or discrete).Logistic regression is basically a supervised classification algorithm. However, the model builds a regression model just like linear regression to predict the probability that a given data entry belongs to the category numbered as “1”.
For example, with binary classification, let ‘x’ be some feature and ‘y’ be the output which can be either 0 or 1.
The probability that the output is 1 given its input can be represented as:
$$p(y=1|x)$$

If we predict the probability via linear regression, we can state it as:
$$p(X) = β0 + β1X
where, p(x) = p(y=1|x)
Logistic regression model can generate the predicted probability as any number ranging from negative to positive infinity, whereas probability of an outcome can only lie between 0< P(x)<1. However, to mitigate the problem of outliers a sigmoid function is used in logistic regression. The linear equation is put in the sigmoid function.
$$g(x) = \frac{1}{1+e^{\smash{-x}}\right}$$

---

## Q: 

**Difficulty:** `Medium`

**Source:** 

[https://careerfoundry.com/en/blog/data-analytics/what-is-logistic-regression/](https://careerfoundry.com/en/blog/data-analytics/what-is-logistic-regression/)

**Answer:**


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
![](https://miro.medium.com/max/963/1*1cFchLVevekWRNRW981Krg.png)

