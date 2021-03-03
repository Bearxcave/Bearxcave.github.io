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
* Mean square error (MSE): 

Scikit-learn, machine learning with python:

```python
from sklearn.family import Model
```

![sklearn cheatsheet](../img/cheatsheet/cheat%20sheet%20scikit-learn.pdf)

### Linear regression

