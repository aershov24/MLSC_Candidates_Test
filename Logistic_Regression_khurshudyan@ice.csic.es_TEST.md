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


 ## **Q: Why can’t linear regression be used in place of logistic regression for binary classification?**

 **Difficulty:** Medium

 **Source:**

 [https://www.upgrad.com/blog/machine-learning-interview-questions-answers-logistic-regression/](https://www.upgrad.com/blog/machine-learning-interview-questions-answers-logistic-regression/)


 **Answer:**

 The reasons why linear regressions cannot be used in case of binary classification are as follows:

 1. Distribution of error terms: The distribution of data in case of linear and logistic regression is different. Linear regression assumes that error terms are normally distributed. In case of binary classification, this assumption does not hold true. 

 1. Model output: In linear regression, the output is continuous. In case of binary classification, an output of a continuous value does not make sense. For binary classification problems, linear regression may predict values that can go beyond 0 and 1. If we want the output in the form of probabilities, which can be mapped to two different classes, then its range should be restricted to 0 and 1. As the logistic regression model can output probabilities with logistic/sigmoid function, it is preferred over linear regression.

 1. Variance of Residual errors: Linear regression assumes that the variance of random errors is constant. This assumption is also violated in case of logistic regression.


 ## **Q: Explain the use of ROC curves and the AUC of an ROC Curve**

 **Difficulty:** Senior

 **Source:**

 [https://www.upgrad.com/blog/machine-learning-interview-questions-answers-logistic-regression/](https://www.upgrad.com/blog/machine-learning-interview-questions-answers-logistic-regression/)

 **Answer:**

 An ROC (Receiver Operating Characteristic) curve illustrates the performance of a binary classification model. It is basically a TPR versus FPR (true positive rate versus false-positive rate) curve for all the threshold values ranging from 0 to 1. In a ROC curve, each point in the ROC space will be associated with a different confusion matrix. A diagonal line from the bottom-left to the top-right on the ROC graph represents random guessing. The Area Under the Curve (AUC) signifies how good the classifier model is. If the value for AUC is high (near 1), then the model is working satisfactorily, whereas if the value is low (around 0.5), then the model is not working properly and just guessing randomly.
