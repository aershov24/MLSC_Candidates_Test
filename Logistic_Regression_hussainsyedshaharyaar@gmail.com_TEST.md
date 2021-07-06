# Topic: Logistic Regression

**Author**: Syed Shaharyaar Hussain

**QAs Total**: 3

---

## Q: If your logistic regression is overfitting then how can you improve model performance?

**Difficulty**: Junior

**Source**: https://towardsdatascience.com/the-basics-logistic-regression-and-regularization-828b0d2d206c

**Answer**: If logistic regression model is overfitting it means on training data it gives good performance but on test data it is not giving as good performance as it gave on training data. This means model has high variance. To counter this issue lasso regularization (L1 Regularization) and ridge regularization (L2 Regularization) can be used for decreasing the model variance that will ultimately decrease the model overfitting. For performing the regularization, we will add regularization terms to our cost function as shown below:

Cost Function:

$$\sum\limits_{i=1}^m(y - y^{(i)})^2$$

Lasso Regularization:

$$\sum\limits_{i=1}^m(y - y^{(i)})^2 + \lambda\sum\limits_{j=0}^p ||\beta_j||$$

Ridge Regularization:

$$\sum\limits_{i=1}^m(y - y^{(i)})^2 + \lambda\sum\limits_{j=0}^p ||\beta_j||^2$$

---

## Q: What are the internal vaildation schemes that can be used in logistic regression to test the effectiveness of model?

**Difficulty**: Mid

**Source**: https://onlinelibrary.wiley.com/doi/full/10.1111/j.1553-2712.2011.01185.x

**Answer**: Following are the internal validation techniques that can be used for testing the effectiveness of logistic model:

1. Test/Train Split
2. k-fold cross-validation
3. Leave-one-out cross-validation
4. Bootstrapping

