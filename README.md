# Introduction to machine learning: half day course
This course provides a short introduction to machine learning. It covers:

- What is machine learning?
- An introduction to unsupervised learning: dimensionality reduction via PCA; and clustering using k-means
- An introduction to supervised learning: linear regression and logistic regression

The course consists of a [lecture](https://htmlpreview.github.io/?https://raw.githubusercontent.com/ben18785/introduction_to_ml/main/presentations/intro_to_ml.html) and a number of problem sets.

There is an introductory problem set which is recommended for all newbies to machine learning:
- [using linear regression to predict house prices](https://htmlpreview.github.io/?https://github.com/ben18785/introduction_to_ml/blob/main/problem_sets/s_applied_regression.nb.html). Here participants apply linear regression modelling and investigate how the model complexity affects its performance on training, validation and testing sets. The dataset used in the problem set is [here](./problem_sets/data/housing_short.csv). The answers to this exercise are in both [R](https://htmlpreview.github.io/?https://github.com/ben18785/introduction_to_ml/blob/main/problem_sets/answers/s_applied_regression.nb.html) and [Python](https://github.com/ben18785/introduction_to_ml/blob/main/problem_sets/answers/s_applied_regression.ipynb).

The following problem sets invite participants to code up a few popular machine learning algorithms:

- unsupervised learning:
  - [*Clustering via k-means*](https://htmlpreview.github.io/?https://github.com/ben18785/introduction_to_ml/blob/main/problem_sets/s_clustering_problems.nb.html). Here, participants code up their own clustering algorithm using the k-means method, which they then apply to the famous [_Iris_](./problem_sets/data/iris.csv) dataset (see the [Wikipedia entry](https://en.wikipedia.org/wiki/Iris_flower_data_set) for a good description of it). The answers (written in R) to this problem set are [here](https://htmlpreview.github.io/?https://github.com/ben18785/introduction_to_ml/blob/main/problem_sets/answers/s_clustering_problems_answers.nb.html).
- supervised learning:
  - [*Linear regression*](https://htmlpreview.github.io/?https://github.com/ben18785/introduction_to_ml/blob/main/problem_sets/s_linear_regression_problems.nb.html). Here, participants train their own linear regression model and investigate how the hyperparameters of gradient descent affect training efficiency. The answers to this problem set are [here](https://htmlpreview.github.io/?https://github.com/ben18785/introduction_to_ml/blob/main/problem_sets/answers/s_linear_regression_problems_answers.nb.html).
  - [*K-nearest-neighbour regression*](https://htmlpreview.github.io/?https://github.com/ben18785/introduction_to_ml/blob/main/problem_sets/s_knn_problems.nb.html). Here, participants code up their own KNN regression model. The answers to this problem set are [here](https://htmlpreview.github.io/?https://github.com/ben18785/introduction_to_ml/blob/main/problem_sets/answers/s_knn_problems_answers.nb.html).


## How to learn more?

All available on Oxford library SOLO:

- "The hundred-page machine learning book", Burkov
- "Hands-On machine learning with Scikit-Learn & Tensorflow", Geron

Coursera:

- [Data Science: Statistics and Machine Learning Specialization, Johns Hopkins](https://www.coursera.org/specializations/data-science-statistics-machine-learning)

## Notes to self for next time I deliver

Reduce the material:

- include levels 1-2 for the "what is ML?" section
- focus only on supervised ML using linear regression and logistic regression

When I gave this course, I actually deviated from the lecture and drew on the screen using Jamboard. In this I had a series of examples:

linear regression:
- house price vs size; how to build a linear model for this; what do the parameters of the linear model mean
- how do we choose the parameters of the linear model? start off with least-squares loss
- how does changing the loss function (e.g. absolute vs 4th power vs square) affect the estimates?
- how do we actually estimate those parameters? For least squares we can estimate the parameters exactly (I don't show this); for other cases, it's generally better to use gradient descent
- explain gradient descent using a 1d graph of the loss function for one of the parameters; talk through why dL/dtheta <0 means that we step in the right direction
- talk about how we can make the model more complex by adding a quadratic term to the regression and show how this results in a curvy line that (may) better fit the data; explain that we can estimate this model via gradient descent
- model complexity: show underfit, fit and overfit models achieved by whatever cap we have on the number of polynomial terms
- training (~70%) / validation (~30%) split: explain that we choose a model of appropriate complexity by training on one set and testing on the validation; as part of this, I plot the loss vs model complexity for both the training and validation sets
- testing set: to avoid overfitting to the training set, we create another set ("testing" ~10%)
