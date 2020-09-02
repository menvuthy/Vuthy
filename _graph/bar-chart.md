---
classes: wide
title: "Python: Side-by-side Bar Chart"
header:
#   image: /assets/images/unsplash-gallery-image-1.jpg
  teaser: images/GraphPlotting/side-by-side-bar-chart/affected-rice.png
categories:
  - Python
tags:
  - Line Chart
  - Stacked Chart

gallery:
  - url: images/GraphPlotting/side-by-side-bar-chart/damage.png
    image_path: images/GraphPlotting/side-by-side-bar-chart/damage.png
    alt: "Data-table-side-by-side-bar-chart"
    title: "Figure 1: Data table for side-by-side bar chart."
gallery1:
  - url: images/GraphPlotting/side-by-side-bar-chart/affected-rice.png
    image_path: images/GraphPlotting/side-by-side-bar-chart/affected-rice.png
    alt: "side-by-side-bar-chart"
    title: "Figure 2: Side-by-side bar chart."
---

Here I will show how to plot Three Stacked Line Graph with the code in Python Jupiter Notebook.


## 1. Data Table

Name data table as: `damage.csv`

{% include gallery caption="Figure 1: Data table for side-by-side bar chart." %}

## 2. Code

```yaml
---
import matplotlib.pyplot as plt
import numpy as np
import pandas as pd
from matplotlib import rc

# set font type
plt.rcParams["font.family"] = "Arial"

# import data table
df = pd.read_csv('damage.csv')

# assign values
xl = np.arange(len(df))
comm = df.iloc[:,0]
aff_rp = df.iloc[:,1]
aff_est = df.iloc[:,2]
dm_rp = df.iloc[:,3]
dm_3t = df.iloc[:,4]
dm_mrc = df.iloc[:,5]

# create plot
plt.figure(figsize=(15,8),constrained_layout=True) 
plt.rc('font', size=20)
plt.rc('xtick', labelsize=20)
plt.rc('ytick', labelsize=22)
plt.rc('axes', labelsize=22)
bar_width = 0.3

plt.grid(which='major',linestyle='--', axis = 'y')
plt.bar(xl, aff_rp,width = bar_width, color = 'tab:red', edgecolor = 'black', label='Affected rice crops from report', zorder = 2)
plt.bar(xl+bar_width, aff_est,width = bar_width, color = 'gray', edgecolor = 'black', label='Affected rice crops from simulation', zorder = 2)
plt.xticks(xl+0.15, comm, rotation = 60)

plt.ylabel('Affected paddy area [ha]', fontsize=22)
plt.xlabel('Name of communes', fontsize=22)
plt.ylim(0,6000)
plt.legend(fontsize = 20)

plt.savefig('affected-rice.png', dpi = 300)
plt.show()
---
```

## 3. Plot

{% include gallery id="gallery1" caption="Figure 2: Side-by-side bar chart plotted in Python." %}

-----

Source code is available at: [GitHub](https://github.com/menvuthy/Code_Collection.git)