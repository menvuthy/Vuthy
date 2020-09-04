---
classes: wide
title: "Python: Comparison of Reported and Estimated Total Damaged Rice Crop"
header:
  teaser: /images/GraphPlotting/total-estimated-damages-rice/total-estimated-damages-rice.png
categories:
  - Python
gallery:
  - url: /images/GraphPlotting/total-estimated-damages-rice/data-table.png
    image_path: /images/GraphPlotting/total-estimated-damages-rice/data-table.png
    alt: "Data-table-total-damaged-rice-crop"
    title: "Figure 1: Data table for total damaged rice crop plot."
gallery1:
  - url: /images/GraphPlotting/total-estimated-damages-rice/total-estimated-damages-rice.png
    image_path: /images/GraphPlotting/total-estimated-damages-rice/total-estimated-damages-rice.png
    alt: "stacked-bar-line"
    title: "Figure 2: Comparison of reported and estimated total damaged rice crop."
---

Here I will show how to plot side-by-side bar with line graph to show the comparison of reported and estimated total damaged rice crop with the code written in Python Jupiter Notebook.

## 1. Data Table

Data source name: `data_table.csv`

{% include gallery caption="Figure 1: Data table for total damaged rice crop plot." %}

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
df_crv = pd.read_csv('data_table.csv')

# assign values
x = np.arange(len(df_crv))
item = df_crv.iloc[:,0]
aff_ha = df_crv.iloc[:,1]
dm_ha = df_crv.iloc[:,2]
dm_er = df_crv.iloc[:,3]
dm_mr = df_crv.iloc[:,4]
dm_lr = df_crv.iloc[:,5]
dm_lr

# create plot
plt.figure(figsize=(8,5.5),constrained_layout=True) 
plt.rc('font', size=18)
plt.rc('xtick', labelsize=18)
plt.rc('ytick', labelsize=18)
plt.rc('axes', labelsize=20)
bw = 0.2

plt.bar(x, aff_ha,width = bw, color = 'grey', edgecolor = 'w', label='Total affected rice', zorder = 2,alpha = 0.8)
plt.bar(x+bw, dm_er,width = bw, color ='#2077B4', edgecolor = 'w', label='Damaged early rice',zorder = 2, alpha = 0.8)
plt.bar(x+bw+bw, dm_mr,width = bw, color = '#B22222', edgecolor = 'w', label='Damaged medium rice', zorder = 2,alpha = 0.8)
plt.bar(x+bw+bw+bw, dm_lr,width = bw, color = '#228B22', edgecolor = 'w', label='Damaged late rice', zorder = 2,alpha = 0.8)
plt.xticks(x+0.3, item)

plt.plot(x+0.3, dm_ha, color ='black', linestyle = '-', marker = 's', markersize = 9, label = 'Total damaged rice')

plt.ylim(0,50)
plt.grid(which='major',linestyle='--', axis = 'y')
plt.ylabel('Rice area [in thousand ha]', fontsize = 20)
plt.xlabel('Type of FDCs', fontsize = 20)
plt.legend(loc = 'upper center', ncol = 2)
plt.text(2.25,2.8 ,'Unable to estimate', fontsize = 18, rotation = 90, color = 'tab:red')

plt.savefig('stacked-bar-line.png', dpi = 300)
plt.show()

---
```

## 3. Plot

{% include gallery id="gallery1" caption="Figure 2: Comparison of reported and estimated total damaged rice crop." %}

-----

Source code is available at: [GitHub](https://github.com/menvuthy/Code_Collection.git)