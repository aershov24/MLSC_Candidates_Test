# Topic: Logistic regression

**Author**: Nigama Vykari Vajjula

**QAs Total:** 3

----

## Q: What is a logistic function and why is it used to model binary data?

**Difficulty:** `Junior`

**Source:** https://machinelearningmastery.com/logistic-regression-for-machine-learning/

**Answer:**

Logistic function an S-shaped curve that can take any real-valued number and map it into a value between 0 and 1, but never exactly at those limits.


![](https://machinelearningmastery.com/wp-content/uploads/2016/03/Logistic-Function.png)

In predictive modeling machine learning projects you are laser focused on making accurate predictions rather than interpreting the results. Logistic functions is most suitable for binary data since it will predict the probability of an instance belonging to the default class, which can be snapped into a 0 or 1 classification. It ensures that the quantity that we are modelling is unbounded.

## Q: What is the difference between PCA and Lasso regression?

**Difficulty:** `Medium`

**Source:** https://stats.stackexchange.com/questions/239518/logistic-regression-with-lasso-versus-pca

**Answer:**

PCA is agnostic to the target variable while LASSO regression isn't, as it is a part of regression model.

PCA can be used as a dimensionality reduction technique if you drop principal components based on a heuristic. But, it offers no feature selection, since the principal components are retained instead of the original features.

![](https://builtin.com/sites/default/files/styles/ckeditor_optimize/public/inline-images/Principal%20Component%20Analysis%20Principal%20Components.png)

LASSO on the other hand, can select parameters through parameter reduction, so as to achieve the purpose of dimensionality reduction. It can intrinsically perform feature selection as the coefficients of predictors are shrunk towards zero. It still requires hyperparameter tuning because there's a regularization coefficient that weighs how severe the regularization of the loss function is.

So feature selection using Lasso regression can be depicted well by changing the regularization parameter.

![](https://miro.medium.com/max/700/1*9gPxjrEAkqWV5tzPEgSkZw.png)

## Q: Explain response variable in a logistic regression and the tricks used to convert it into an mathematical equation.

**Difficulty:** `Senior`

**Source:** http://csugar.bol.ucla.edu/Courses/201afall2011/exams/finalpracsoln.pdf

**Answer:**

In a logistic regression the response variable, Y, is an indicator saying whether or not you have a particular characteristic, say lung cancer. The problem is that the value of an indicator is always 1 or 0. This is how we turn something qualitative into something quantitative.

Unfortunately a model of the form $$β_{0} + β_{1}X_{1} + β_{2}X_{2}$$ doesn't produce values that are exactly 0 or 1. Thus instead we focus on modeling the probability that is either Y=0 or Y=1. This isn’t quite good enough as the probability is between 0 and 1, and there is no certainty that $$β_{0} + β_{1}X_{1} + β_{2}X_{2}$$ will lie in that range.

Therefore, we do one more trick which is to take the odss that Y=1, given by $$ \frac {P(Y = 1)}{P(Y = 0)}$$ and take the log to get a number between negative and positive infinity. This is the number we model using our standard regression formula.
