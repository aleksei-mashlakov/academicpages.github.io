---
title: 'On the interactive visualization of multivariate time series data'
date: 2023-01-28
permalink: /posts/2023/01/visualization-plotly/
classes: wide
layout: single
tags: 
  - python
  - visualization
---
> 5 ways to visualise the data with plotly based on M6 competition data

In this story I diving into the visualization of multivariate time series data. The following analysis are described here to investigate the properties of multivariate time series data:


### First things first

To set up the analysis environment, we start by importing the necessary dependencies.

<script src="https://gist.github.com/aleksei-mashlakov/3ad26154dcf027c6b36dce40e02e288e.js"></script>

{% include plotly/figure_29.html %}


```python
import matplotlib.pyplot as plt
import numpy as np
from scipy.signal import convolve2d
# read image
image = np.array(Image.open("path/to/file.jpg").convert('L'))
# apply convolution
kernel = np.array([[-1, -1, -1],
                   [ 0,  0,  0],
                   [+1, +1, +1]])
conv_output = convolve2d(image, kernel, mode='same')
# display
plt.figure(figsize=(15,5))
plt.subplot(121), plt.imshow(image, cmap='gray'), plt.axis('off')
plt.subplot(122), plt.imshow(np.abs(conv_output), cmap='gray'), plt.axis('off')
plt.tight_layout()
plt.show()
```

[![Generic badge](https://img.shields.io/badge/License-MIT-blue.svg?style=plastic)](https://lbesson.mit-license.org/) [![Generic badge](https://img.shields.io/badge/acces_au_code-github-black.svg?style=plastic&logo=github)](https://github.com/julienguegan/notebooks_blog/blob/main/visualisation_CNN.ipynb)