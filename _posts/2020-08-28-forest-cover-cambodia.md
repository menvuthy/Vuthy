---
classes: wide
title: "Cambodia: Forest Cover Change in 21st Century"
tagline: "This visualization is based on high-resolution global forest cover data developed by Hansan et al (2013)."
header:
  overlay_image: /images/forest-cambo/homepage_img.jpg
categories:
  - Global Forest Cover
tags:
  - Cambodia
  - Forest Cover
  - QGIS
  - Earth Engine API
last_modified_at: 2020-08-28
gallery:
  - url: /images/forest-cambo/global-forest-cover.jpg
    image_path: /images/forest-cambo/global-forest-cover.jpg
    alt: "global-forest-cover"
    title: "Figure 1a: Global Forest Cover in 2000"
  - url: /images/forest-cambo/global-forest-loss.jpg
    image_path: /images/forest-cambo/global-forest-loss.jpg
    alt: "global-forest-cover-loss"
    title: "Figure 1b: Global Forest Cover Loss from 2000 to 2019"
# gallery1:
#   - url: /images/forest-cambo/FC_2000.jpg
#     image_path: /images/forest-cambo/FC_2000.jpg
#     alt: "Forest Cover in 2000"
#     title: "Figure 2a: Forest Cover in 2000"
#   - url: /images/forest-cambo/FC_2019.jpg
#     image_path: /images/forest-cambo/FC_2019.jpg
#     alt: "Forest Cover in 2019"
#     title: "Figure 2b: Forest Cover in 2019"
---
<!-- global-forest-loss.jpg -->

Forest cover plays an essential role in delivering important ecosystem services, including biodiversity richness, climate regulation, carbon storage, and water supplies (1). However, spatially and temporally detailed information on global-scale forest cover changes at a high resolution did not exist until M.C. Hansen and his team in the University of Maryland, USA developed a global-scale forest change and published the works in 2013 (2). Hansen et al (2) mapped global tree cover extent, loss, and gain annually for the period from 2000 to 2012 at a spatial resolution of 30 m, especially the datasets have been updated every year. Importance of data for practical engineering.
Therefore, here I will illustrate one of many remote sensing methods to extract the datasets to:
{: style="text-align: justify;"}

1. Visualize the global forest cover in 2000, and forest cover loss during the period 2000-2019. 
2. Examine the spatial and temporal changes of both forest cover loss and gain in Cambodia from 2000 to 2019.
3. Calculate the yearly forest loss in Cambodia from 2000 to 2019.


## Global Forest Cover and Loss

In this dataset, there are four important definitions as following:
* **Trees** are defined as vegetation taller than 5m in height and are expressed as a percentage per output grid cell.
* **Forest Cover Loss** is defined as a stand-replacement disturbance, or a change from a forest to non-forest state, during the period 2000–2019. 
* **Forest Cover Gain** is defined as the inverse of loss, or a non-forest to forest change entirely within the period 2000–2012. 
* **Forest Loss Year** is a disaggregation of total ‘Forest Loss’ to annual time scales.
{: style="text-align: justify;"}

{% include gallery caption="Figure 1: (a) Global forest cover in 2000 (left). (b) Global forest cover loss from 2000 to 2019 (right)" %}

## Forest Cover Loss and Gain in Cambodia

Here is the comparison image of forest cover between 2000 and 2019 of the whole country.

<!-- {% include gallery1 caption="Figure 2: (a) Forest cover in 2000 (left). (b) Forest cover in 2019 (right)" %} -->

Video showing spatial and temporal changes of forest cover in Cambodia from 2000 to 2019.

<iframe width="1280" height="720" src="https://www.youtube.com/embed/4D_sMds61jY" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

   
 
By only viewing the video, the forest cover loss of some areas are exaggerated due to the far view of image and also the low density of forest canopy; hence, it is important to zoom into some specific areas to have a closer view of the forest cover and loss. 




## Reference
1. Foley, Jonathan A., et al. "Global consequences of land use." science 309.5734 (2005): 570-574.
2. Hansen, Matthew C., et al. "High-resolution global maps of 21st-century forest cover change." science 342.6160 (2013): 850-853.