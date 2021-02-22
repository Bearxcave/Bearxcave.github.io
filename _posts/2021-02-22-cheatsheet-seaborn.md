---
layout:     post
title:      Cheatsheet for Seaborn
subtitle:   Seaborn command
date:       2021-02-22
author:     Bearx
header-img: img/post-bg-grand-canyon.jpg
catalog: true
tags:
    - cheatsheet
---

### Cheatsheet for Seaborn basic

Import seaborn package and set the sns theme:
```python
import seaborn as sns
sns.set_theme()
```

Load data and plot:
```python
df = sns.load_dataset('data_file')
sns.distplot(df['column_name'],kde=False,bins=30) # Deprecated in future version

sns.displot(df['column_name']) # Use this or the following command \\
sns.histplot(df['column_name'])

sns.jointplot(x='column_1',y='column_2',data=df,kind='scatter') # Scatter joint plot  
sns.jointplot(x='column_1',y='column_2',data=df,kind='hex') # Hex joint plot
sns.jointplot(x='column_1',y='column_2',data=df,kind='reg') # Regression joint plot
sns.jointplot(x='column_1',y='column_2',data=df,kind='kde') # 2-D KDE joint plot

sns.pairplot(df,hue='column_category',palette='coolwarm')

sns.rugplot(df['column_name'])
sns.kdeplot(df['column_name']) # Kernel Density Estimation plots
```
