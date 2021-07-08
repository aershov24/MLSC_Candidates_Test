# Logistic Regression

#### Presented by: Ayesha Siddiqa
___

## Q: Why is logistic regression called regression and not classification?
**Difficulty Level:** ```Junior```

[Source](https://towardsdatascience.com/understanding-logistic-regression-9b02c2aec102)

**Answer:**

Logistic regression is basically a supervised classification algorithm. The term “Logistic” is taken from the Logit function that is used to solve a classification problem. It is named Logistic "Regression" because its underlying technique is quite the same as Linear Regression. The main difference between regression and classification is that the output variable in regression is numerical or continuous while that for classification is categorical or discrete.

___

## Q: In Machine Learning, What is over-fitting and under-fitting concepts? How can we avoid over-fitting and under-fitting in regression models?
**Difficulty Level:** ```Medium```

[Source](https://machinelearningmastery.com/overfitting-and-underfitting-with-machine-learning-algorithms/)

**Answer:**

### Over-fitting

Over-fitting occurs when the model sort of memorizes the complex patterns in target classes in data instead of generalizing them. This means a model learns the detail and noise in the training data to the extent that it negatively impacts the performance of the model on new data. So, the model starts memorizing the training set which literally doesn’t work when unseen data is fed.

### Under-fitting

Under-fitting refers to a model that can neither model the training data nor generalize to new data. An underfit machine learning model is not a suitable model and will be obvious as it will have poor performance on the training data.

![Over-Fit, Under-fit & a Good-fit Model](https://miro.medium.com/max/1125/1*_7OPgojau8hkiPUiHoGK_w.png)

### Over-fitting Limitations
#### Adding more data
The model is overfitting when it fails to generalize to new data. That means the data it was trained on is not representative of the data it is meeting in production. So, retraining your algorithm on a bigger, richer and more diverse data set should improve its performance.

#### Data augmentation
This is a set of techniques used to artificially increase the size of a dataset by applying transformations to the existing data. 

#### Regularization
The main concept of regularization is that these techniques introduce a “complexity penalty” to your model. If the model wants to avoid incurring that penalty, it needs to focus on the most prominent patterns which have a better chance of generalizing well.

#### Removing features from data
Sometimes, model may fail to generalize simply because the data it was trained on was too complex and the model missed the patterns it should have detected. Removing some features and making your data simpler can help reduce overfitting.

### Under-fitting Limitations

#### Increasing the model complexity
Model may be underfitting simply because it is not complex enough to capture patterns in the data. Using a more complex model, will very often help solve underfitting.

#### Adding features to training data
 Model may be underfitting because the training data is too simple. Adding features and complexity to your data can help overcome underfitting.

---

## Q: What is the key difference between ridge and lasso regressions? And describe when to use these regularization?

**Difficulty Level:** ```Senior```

[Source](https://discuss.analyticsvidhya.com/t/difference-between-ridge-regression-and-lasso-and-its-effect/3000)

**Answer:**

| Ridge Regression          | Lasso Regression          |
|---------------------------|---------------------------|
|1.  Ridge uses l2 function.|1. Whereas lasso go with l1 function.|
|2.  Ridge regression adds “squared magnitude” of coefficient as penalty term to the loss function.|2. whereas Lasso Regression adds “absolute value of magnitude” of coefficient as penalty term to the loss function.|
|3. Ridge never sets the value of coefficient to absolute zero.|3. Lasso regression tends to make coefficients to absolute zero.|
|4. In Ridge Regression you either select all the coefficients or none of them.|4. While Lasso does both parameter shrinkage and variable selection automatically because it zero out the co-efficients of collinear variables.

### Usage of Ridge Regression
Ridge regression is the method used for the analysis of multicollinearity in multiple regression data. It is most suitable when a data set contains a higher number of predictor variables than the number of observations. The second-best scenario is when multicollinearity is experienced in a set.

### Usage of Lasso Regression
This particular type of regression is well-suited for models showing high levels of multicollinearity or when you want to automate certain parts of model selection, like variable selection/parameter elimination.

___

This is the end of the article, but the learning and growing journey continues. Stay tuned.... :) 