---
layout:     post
title:      Cheatsheet for Plotly
subtitle:   Plotly command
date:       2021-03-02
author:     Bearx
header-img: img/post-bg-grand-canyon.jpg
catalog: true
tags:
    - cheatsheet
---

### Cheatsheet for Plotly basic

Plotly is an interactive plotting tool.

Initialize Plotly in this way:
```python
import pandas as pd
import numpy as np

import cufflinks as cf
from plotly.offline import download_plotlyjs, init_notebook_mode, plot, iplot
init_notebook_mode(connected=True)
cf.go_offline()
```

Possible plotting methods using Plotly:
* scatter
* bar
* box
* spread
* ratio
* heatmap
* surface
* histogram
* bubble
Here is some examples:
```python
df.iplot(kind='scatter',x='A',y='B',mode='markers',size=10)

df = pd.DataFrame({'x':[1,2,3,4,5],'y':[10,20,30,20,10],'z':[5,4,3,2,1]})
df.iplot(kind='surface',colorscale='rdylbu')
```

One more plotting method, `scatter_matrix()`, is similar to `sns.pairplot()`:
```python
df.scatter_matrix()
```

### Plotly provides various plotting methods for geographical plotting
```python
import chart_studio.plotly as py
import plotly.graph_objs as go 
from plotly.offline import download_plotlyjs, init_notebook_mode, plot, iplot
init_notebook_mode(connected=True) 
```
