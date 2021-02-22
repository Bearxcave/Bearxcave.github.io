---
layout:     post
title:      Cheat Sheets for Seaborn
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
```
import seaborn as sns
sns.set_theme()
```

Load data and plot:
```
df = sns.load_dataset('data_file')
sns.displot(df['column_name'])
```
