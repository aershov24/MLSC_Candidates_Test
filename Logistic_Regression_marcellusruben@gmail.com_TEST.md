# Topic: Logistic Regression

**Author**: Ruben Winastwan

**QAs Total**: 3

---
## Q: Could you explain what Logistic Regression is and when should we use it?
**Difficulty:** `Junior`

**Source**:

https://www.analyticsvidhya.com/blog/2021/05/20-questions-to-test-your-skills-on-logistic-regression/

**Answer**:

Logistic Regression is a classification algorithm that is used where the target variable is of categorical nature. The main objective behind Logistic Regression is to determine the relationship between features and the probability of a particular outcome.

For example, when we need to predict whether a student passes or fails in an exam given the number of hours spent studying as a feature, the target variable comprises two values i.e. pass and fail.

---
## Q: What can you infer from each of the hand drawn decision boundary of Logistic Regression below? Also, what should we do to fix the problem of each decision boundary? 
![DB](https://raw.githubusercontent.com/marcellusruben/Misc/main/Qc281.jpg)

**Difficulty:** `Medium`

**Source**:

https://www.analyticsvidhya.com/blog/2017/08/skilltest-logistic-regression/

**Answer**:

What can we infer:
- Left: the model underfits the data. It will give us the maximum error compared to other two models.
- Center: best fitting model.
- Right: the model overfits the data. It performs exceptionally well on training data but performs considerably worse on test data.

What can we do to fix the problem:
- Left: increase the complexity of the model or increase the number of independet variables.
- Center: best performing model, so we don't need to tweak anything.
- Right: add regularization method to the model.

---

## Q: Imagine that you know there are outliers in your data, would you use Logistic Regression as your model? If yes, why? If not, could you recommend a better model?

**Difficulty:** `Senior`

**Source**:

- https://www.analyticsvidhya.com/blog/2021/05/20-questions-to-test-your-skills-on-logistic-regression/
- https://www.elderresearch.com/blog/jump-start-your-modeling-with-random-forests/

**Answer**:

**Logistic Regression:** Logistic Regression is an algorithm that will be highly influenced by outliers. If we have outliers in our dataset, the decision boundary could be shifted, which will lead to incorrect inferences. So using Logistic Regression wouldn't be optimal if we have outliers.

**Tree-based model:** Algorithms like decision tree or random forest are more robust to outliers. This is because unlike linear model like Logistic Regression, tree-based model works by splitting the data into groups (repeatedly) according to whether a data point is above or below a selected threshold value on a selected feature variable. Thus, a data point with much higher value than the rest wouldn't influence the decision of tree-based model at all.












 

