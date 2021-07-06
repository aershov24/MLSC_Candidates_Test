Note: Please use light theme otherwise some of the images may not be clearly visible.

# Topic: Logistic Regression

**Author**: Syed Shaharyaar Hussain

**QAs Total**: 3

---

## Q: If your logistic regression is overfitting then what parametric techniques you can use to improve model performance?

**Difficulty**: Junior

**Sources**: 
1. https://towardsdatascience.com/the-basics-logistic-regression-and-regularization-828b0d2d206c
2. https://scikit-learn.org/stable/modules/cross_validation.html

**Answer**: If logistic regression model is overfitting it means on training data it gives good performance but on test data it is not giving as good performance as it gave on training data. This means model has high variance. To counter this issue lasso regularization (L1 Regularization) and ridge regularization (L2 Regularization) can be used for decreasing the model variance that will ultimately decrease the model overfitting. For performing the regularization, we will add regularization terms to our cost function as shown below:

Cost Function:

$$\sum\limits_{i=1}^m(y - y^{(i)})^2$$

Lasso Regularization:

$$\sum\limits_{i=1}^m(y - y^{(i)})^2 + \lambda\sum\limits_{j=0}^p ||\beta_j||$$

Ridge Regularization:

$$\sum\limits_{i=1}^m(y - y^{(i)})^2 + \lambda\sum\limits_{j=0}^p ||\beta_j||^2$$

---

## Q: What are the internal vaildation schemes that can be used in logistic regression to test the effectiveness of model?

**Difficulty**: Medium

**Source**: https://onlinelibrary.wiley.com/doi/full/10.1111/j.1553-2712.2011.01185.x

**Answer**: Following are the internal validation techniques that can be used for testing the effectiveness of logistic model:

### 1. Test/Train Split
Here, we simply divide the data into train and test set.

### 2. k-fold cross-validation
In k-cross validation we divide the training dataset into k-sets or k-folds in which k-1 folds are used for training the model and remaining one fold is used for testing the model with given hyperparamters. Once we select the model with the best hyperparameters then we run that model on our test dataset. Benefit of k-cross validation is that it can help in determining the best parameters for the model. Moreover k-fold cross-validation is better compared to test/validation/test split.

#### Pipeline:
![image](https://user-images.githubusercontent.com/32700434/124615602-dd08dd00-de8e-11eb-9d8d-c21ccc00cfad.png)

#### K-fold cross-validation scheme:
![image](https://user-images.githubusercontent.com/32700434/124613420-a29e4080-de8c-11eb-859f-a0fb504b8026.png)

### 3. Leave-one-out cross-validation
It is a variant of k-fold cross-validation in which number of folds "k" equals the number of samples "N" present in the data set. In the end we take the average accuracy as a result.

### 4. Bootstrapping
In bootstrapping, we randomly take repeated sub-samples from the same dataset and evaluate the model performance. In the end, we take the average accuracy as a result.
