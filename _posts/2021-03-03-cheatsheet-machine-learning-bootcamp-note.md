---
layout:     post
title:      Machine learning note
date:       2021-03-03
author:     Bearx
header-img: img/post-bg-grand-canyon.jpg
catalog: true
tags:
    - note
    - machine learning
---

### List of PDF cheatsheets

* pandas: [pandas](../img/cheatsheet/cheat%20sheet%20pandas.pdf)
* plotly: [plotly](../img/cheatsheet/cheat%20sheet%20plotly.pdf)
* scikit-learn: [sklearn](../img/cheatsheet/cheat%20sheet%20scikit-learn.pdf)

### Basic

Data is often split into 3 sets:

* Training data
* Validation data
* Test data

Classification error metrics:

* Accuracy
* Recall
* Precision
* F1-Score : $2 \frac{\mathrm{precision}*\mathrm{recall}}{\mathrm{precision}+\mathrm{recall}}$

Confusion matrix:

|                    | Prediction positive | Prediction negative |
|:------------------:|:-------------------:|:-------------------:|
| Condition positive | True positive (TP)  | False negative (FN) |
| Condition negative | False positive (FP) | True negative (TN)  |

Regression error metrics:

* Mean absolute error (MAE): easy to be affected by large errors
* Mean square error (MSE)
* Root Mean Squared Error (RMSE)

Bias variance trade-off:

* underfitting: high bias, low variance
* overfitting: low bias, high variance

### Linear regression

### Logistic regression

### K-nearest network (KNN)

Training algorithm:

1. Store all the data

Prediction algorithm:

1. Calculate the distance from x to all points in the data
2. Sort the distances
3. Predict the majority label of the "k" closest points

### Tree methods

* Decision Tree
* Random forest

### Support Vector Machine (SVM)

### K Means Clustering

Algorithm:

1. Choose a number of Clusters "K"
2. Randomly assign each point to a cluster
3. Repeat the following until converged:
    * For each cluster, compute the cluster centroid by taking the mean vector of points in the cluster
    * Assign each point to the cluster for which the centroid is the closest

Elbow method (to estimate K):

1. Compute the sum of squared error (SSE) for a list of K's: $ W(C_k) = \frac{1}{\mathrm{abs}(C_k)} \sum_{i,i'\in C_k} \sum_{j=1}^p (x_{ij}-x_{i'j})^2 $
2. Plot SSE against K, and figure the elbow point

