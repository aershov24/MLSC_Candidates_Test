## Q: What is a logistic function and why is it used to model binary data? 

**Difficulty:** `Junior`

**Source:** https://machinelearningmastery.com/logistic-regression-for-machine-learning/

**Answer:**

## Q: What is the difference between PCA and Lasso regression?

**Difficulty:** `Medium`

**Source:** https://stats.stackexchange.com/questions/239518/logistic-regression-with-lasso-versus-pca

**Answer:**

## Q: How do you detect and rectify the problem of heteroscedasticity? 

**Difficulty:** `Senior`

**Source:** https://www.glassdoor.co.nz/Interview/what-is-heteroscedasticity-in-regression-how-will-you-solve-it-in-a-practical-situaion-model-evaluation-and-comments-bas-QTN_4431327.htm

**Answer:**

There are several methods of testing for the presence of heteroscedasticity. The most commonly used is the Time-Honored Method of Inspection (THMI). This test involves looking for patterns in a plot of the residuals from a regression. Two more formal tests are White's General test (White 1980) and the Breusch-Pagan test (Breusch and Pagan 1979).
The White test is computed by finding nR2 from a regression of ei2 on all of the distinct variables in X \otimes X, where X is the vector of dependent variables including a constant. This statistic is asymptotically distributed as chi-square with k-1 degrees of freedom, where k is the number of regressors, excluding the constant term.

The Breusch-Pagan test is a Lagrange multiplier test of the hypothesis that the independent variables have no explanatory power on the ei2's. If u equals (e12, e22, . . . , en2), i equals an n ×1 column of ones, and \bar u=e^' e/n, then Koenkar and Bassett's (1982) robust variance estimator

V=\frac{1}n \sum_{i=1}^n {( 2e_i - \frac{e^' e}n )^2}
computes the test statistic as
LM=( \frac{1}V ) (u - \hat u i)^' Z(Z^' Z)^{-1}Z^'(u - \hat u i)
which is asymptotically distributed as chi-square with degrees of freedom equal to the number of variables in Z.


