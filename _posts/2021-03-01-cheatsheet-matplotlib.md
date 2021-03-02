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

Configuration for multiple subplots:
```python
fig = plt.figure()
ax1 = fig.add_subplot(211)
ax2 = fig.add_subplot(212)

# Or initialize in this way:


fig, ax = plt.subplots(1, 2, gridspec_kw={'width_ratios': [2, 5]})
pp1 = ax[0].imshow(matrix_plotted, cmap='hot')
pp2 = ax[1].scatter(x, y, c=v, cmap='hsv', s=marker_size)

ax[0].set_ylim(-1, 1)
ax[1].set_xticks(np.array(range(NP))*ND2-0.5)
ax[1].set_yticks(np.array(range(NP))*ND2-0.5)
ax[1].set_title('t='+'%5.4f'%(t_history[t_index]))
plt.grid(True)

pp1.set_clim(0,1)
pp2.set_clim(0,1)
plt.colorbar(pp1)

fig.set_size_inches(14, 10)
plt.show()

```
