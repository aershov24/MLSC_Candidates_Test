# Topic: Logistic Regression

**Author**: Ruben Winastwan

**QAs Total**: 3

---
## Q: Could you explain what Logistic Regression is and when should we use it? Why should we use Logistic Regression instead of Linear Regression?
**Difficulty:** `Junior`

**Source**:

https://towardsdatascience.com/logistic-regression-detailed-overview-46c4da4303bc

**Answer**:

Logistic Regression is used when the dependent variable(target) is categorical.

For example, to predict whether an email is spam (1) or not (0).

Consider a scenario where we need to classify whether an email is a spam or not. The output that we need is either 1 (spam) or 0 (non-spam). No other values in between. Linear regression will generate output that is continuous and unbounded and thus, wouldn't be suitable for this scenario. Logistic Regression, however, uses a sigmoid function to map our output into a value between 0 to 1. The next thing that we need to do is setting a threshold value to classify an email as a spam or not, let's say 0.5. If the output then below 0.5, then Logistic Regression will classify the email as non-spam and vice-versa.  

---
## Q: What can you infer from each of the hand drawn decision boundary of Logistic Regression below? Also, what should we do to fix the problem of each decision boundary? 
![DB](https://raw.githubusercontent.com/marcellusruben/Misc/main/Qc281.jpg)

**Difficulty:** `Medium`

**Source**:

- https://www.analyticsvidhya.com/blog/2017/08/skilltest-logistic-regression/
- Page 27-29 of Hands-On Machine Learning with Scikit-Learn, Keras, & TensorFlow book by Aurelien Geron.
- Personal experience.

**Answer**:

What can we infer:
- Image A: the model underfits the data. It will give us the maximum error on training data compared to other two models.
- Image B: best fitting model.
- Image C: the model overfits the data. It performs exceptionally well on training data but performs considerably worse on test data.

What can we do to fix the problem:
- Image A: increase the complexity of the model or increase the number of independent variables by doing feature engineering.
- Image B: best performing model, so we don't need to tweak anything.
- Image C: add regularization method to the model.

---

## Q: Imagine that you know there are outliers in your input data, would you use Logistic Regression as your model? If yes, why? If not, could you recommend a better model?

**Difficulty:** `Senior`

**Source**:

- https://stats.stackexchange.com/questions/279010/how-does-outlier-impact-logistic-regression
- https://datascience.stackexchange.com/questions/37394/are-decision-trees-robust-to-outliers/37402
- Personal experience

**Answer**:

**Logistic Regression:** Logistic Regression is an algorithm that will be highly influenced by outliers. If we have outliers in our dataset, the decision boundary could be shifted, which will lead to incorrect inferences. This will lead to a model that is prone of making a Type I error or Type II error. In other words, we couldn't trust the inference made by our Logistic Regression model. Hence, using Logistic Regression wouldn't be optimal if we have outliers in our input data.

**Tree-based model:** Algorithms like decision tree or random forest are more robust to outliers compared to Logistic Regression. This is because unlike linear model like Logistic Regression, tree-based model works by splitting the data into groups (repeatedly) according to whether a data point is above or below a selected threshold value on a selected feature variable. Thus, a data point with much higher value than the rest wouldn't influence the decision of tree-based model at all.












 

