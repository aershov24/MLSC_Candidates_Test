# Topic: Logistic Regression

**Author**: Poetri Heriningtyas

**QAs Total**: 3

---

## Q: Why is logistic regression called regression and not classification?

**Difficulty:** `Junior`

**Source:**

* https://www.fharrell.com/post/classification/
* https://ryxcommar.com/2020/06/27/why-do-so-many-practicing-data-scientists-not-understand-logistic-regression/

**Answer:**

Classification is when you make a concrete determination of what category something is a part of. Binary classification involves two categories, and by the law of the excluded middle, that means binary classification is for determining whether something “is” or “is not” part of a single category. There either are children playing in the park today (1), or there are not (0).

Although the variable you are targeting in logistic regression is a classification, logistic regression does not actually individually classify things for you: it just gives you probabilities (or log odds ratios in the logit form). The only way logistic regression can actually classify stuff is if you apply a rule to the probability output. For example, you may round probabilities greater than or equal to 50% to 1, and probabilities less than 50% to 0, and that’s your classification.


---

## Q: How will you deal with the multiclass classification problem using Logistic Regression?

**Difficulty:** `Medium`

**Source:**

https://chrisyeh96.github.io/2018/06/11/logistic-regression.html

**Answer:**

There are two common approaches to use them for multi-class classification: **one-vs-rest** (also known as **one-vs-all**) and **one-vs-one**. Each has its strengths and weaknesses. There is no clear “best” multi-class classification model; it depends on the dataset.

In **one-vs-rest**, we train <img src="https://render.githubusercontent.com/render/math?math=C"> separate binary classification models. Each classifier <img src="https://render.githubusercontent.com/render/math?math=f_c">, for <img src="https://render.githubusercontent.com/render/math?math=c\in\{1,...C\}"> is trained to determine whether or not an example is part of class <img src="https://render.githubusercontent.com/render/math?math=c"> or not. To predict the class for a new example <img src="https://render.githubusercontent.com/render/math?math=x">, we run all <img src="https://render.githubusercontent.com/render/math?math=C"> classifiers on <img src="https://render.githubusercontent.com/render/math?math=x"> and choose the class with the highest score: <img src="https://render.githubusercontent.com/render/math?math=\hat{y} = argmax_{c\in\{1,...C\}} f_c(x)">. One main drawback is that when there are lots of classes, each binary classifier sees a highly imbalanced dataset, which may degrade performance.

In **one-vs-one**, we train <img src="https://render.githubusercontent.com/render/math?math={C \choose 2} = C(C-1)/2)"> separate binary classification models, one for each possible pair of classes. To predict the class for a new example <img src="https://render.githubusercontent.com/render/math?math=x">, we run all <img src="https://render.githubusercontent.com/render/math?math={C \choose 2}"> classifiers on <img src="https://render.githubusercontent.com/render/math?math=x"> and choose the class with the most “votes.” A major drawback is that there can exist fairly large regions in the decision space with ties for the class with the most number of votes.


---
## Q: Why don’t we use `Mean Squared Error as a cost function in Logistic Regression?

**Difficulty**: `Senior`

**Source:**

https://www.analyticsvidhya.com/blog/2020/11/binary-cross-entropy-aka-log-loss-the-cost-function-used-in-logistic-regression/

**Answer:**

In linear regression, we used the squared error mechanism. Unfortunately for logistic regression, such a cost function produces a nonconvex space that is not ideal for optimization. There will exist many local optima on which our optimization algorithm might prematurely converge before finding the true minimum.