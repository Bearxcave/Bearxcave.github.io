---
layout:     post
title:      Cheatsheet for Pandas
subtitle:   Pandas command
date:       2021-02-20
author:     Bearx
header-img: img/post-bg-grand-canyon.jpg
catalog: true
tags:
    - cheatsheet
---

### Cheatsheet for Pandas basic

Basic operation on Pandas dataframe:
```python
import pandas as pd
df = pd.read_csv('data_frame.csv')

df.head()
df.info()

df['column_name'].mean()
df['column_name'].max()
df['column_name'].min()

df['column_name'].unique()
df['column_name'].nunique()

df['column_name'].count()
df['column_name'].value_counts().head(10)

df['column_name'].apply(user_defined_func)
df[['column_name_1','column_name_2']].corr()
```

Built-in data visualization
```python
df['column_name'].hist(bins=30) # or

df['column_name'].plot(kind='hist',bins=30) # or

df['column_name'].plot.hist(bins=30)

# Area plot

df['column_name'].plot.area(alpha=0.5)

# 
```
