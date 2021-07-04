## **Topic: Logistic Regression**

**Author:** Martiros Khurshudyan

**QAs Total:** 3

## **Q: What is decision boundary in Logistic Regression?**

**Difficulty:** Junior

**Source:**

[https://towardsdatascience.com/logistic-regression-detailed-overview-46c4da4303bc](https://towardsdatascience.com/logistic-regression-detailed-overview-46c4da4303bc)

**Answer:**

To predict which class a data belongs, a threshold can be set. Based upon this threshold, the obtained estimated probability is classified into classes.
Say, if predicted_value ≥ 0.5, then classify email as spam else as not spam.
Decision boundary can be linear or non-linear. Polynomial order can be increased to get complex decision boundary.


## **Q: Do we need to standardize the values present in the feature columns before we feed the data into a training logistic regression model?**

**Difficulty:** Medium

**Source:**

[https://www.kodlogs.com/interview/blog/125/commonly-logistic-regression-questions-answers-interview](https://www.kodlogs.com/interview/blog/125/commonly-logistic-regression-questions-answers-interview)

**Answer:**

No, we do not need to standardize the values present in the feature space, which we have to use to train the logistic regression model. So, the answer to this question would be FALSE. We choose to standardize all our values to help the function (usually gradient descent), which is responsible for making the algorithm converge on a value. Since this algorithm is relatively simple, it does not need the amounts to be scaled for it actually to have a significant difference in its performance.


## **Q: Explain how to use Standard Deviation for Anomalies Detection?**

**Difficulty:** Senior

**Source:**

[https://towardsdatascience.com/5-ways-to-detect-outliers-that-every-data-scientist-should-know-python-code-70a54335a623](https://towardsdatascience.com/5-ways-to-detect-outliers-that-every-data-scientist-should-know-python-code-70a54335a623)

**Answer:**
