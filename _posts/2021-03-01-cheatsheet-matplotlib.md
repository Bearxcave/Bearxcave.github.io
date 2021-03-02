---
layout:     post
title:      Cheatsheet for Matplotlib
subtitle:   Matplotlib command
date:       2021-03-01
author:     Bearx
header-img: img/post-bg-grand-canyon.jpg
catalog: true
tags:
    - cheatsheet
---

### Cheatsheet for Matplotlib basic

Configuration for a single plot:
```python
plt.plot(data_x, data_y, 'k.-')

plt.grid(True)
plt.ylim(y_min, y_max)
plt.title('Here is the title')
fig = plt.gcf()
fig.set_size_inches(14, 5)
plt.show()
```
