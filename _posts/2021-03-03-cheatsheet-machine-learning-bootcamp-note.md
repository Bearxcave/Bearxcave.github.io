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

Cheatsheet for Scikit-learn: [sklearn cheatsheet](../img/cheatsheet/cheat%20sheet%20scikit-learn.pdf)

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


