---
title: "Phnom Penh: Urban Growth from 1988 to 2020 by Landsat Satellite Imagery"
tagline: "This timelapse image reveals 33-year growth of Phnom Penh city."
header:
  overlay_image: /images/pp-growth/head-image.png
  caption: "Photo credit: [**Photopea**](https://photopea.com)"
categories:
  - Layout
  - Uncategorized
tags:
  - edge case
  - image
  - layout
last_modified_at: 2020-08-12
permalink: /newsfeed/
---
# Phnom Penh City: 1988 - 2020
More than thirty years ago, buildings and streets were barely on the map of Phnom Penh city. In 1988 it was home to approximately 615,000 people; however, 33 years later that had risen to more than 2 million according to worldpopulationreview.com.


<img src="{{ site.url }}{{ site.baseurl }}/images/pp-growth/pp-collage.jpg" alt="">
<figure>
  {{ fig_img | markdownify | remove: "<p>" | remove: "</p>" }}
  <figcaption>Phnom Penh city in 1988 (population ~615,000) and 2020 (population ~2,080,000).</figcaption>
</figure>

The yearly images were produced from the images of Landsat Satellite 5, 7 and 8 aiming at illustrating the spatial and temporal changes of urban growth in Phnom Penh city from 1988 to 2020.

Here is the **Timelapse of Phnom Penh city** (1987 - 2020):
<img src="{{ site.url }}{{ site.baseurl }}/images/pp-growth/pp-growth.gif" alt="">
<figure>
  {{ fig_img | markdownify | remove: "<p>" | remove: "</p>" }}
  <figcaption>Phnom Penh city from 1987 to 2020.</figcaption>
</figure>

## Landsat Processing Methods

The development of image for each year was performed in Jupiter Notebook without having to download any image collection from the satellite's website and resort to any GIS Desktop software. The entire geoprocessing and remote sensing routine requires use `Earth Engine Python API` and `geemap`. The geemap Python package is built upon the `ipyleaflet` and `folium` packages and implements several methods for interacting with Earth Engine data layers, such as `Map.addLayer()`, `Map.setCenter()`, and `Map.centerObject()`. Below are the main steps to develop the image:
1. Install `Earth Engine Python API` and `geemap` based on the guidline in `https://geemap.readthedocs.io/en/latest/`
2. Import `geemap package` into Python
3. Create an interactive map (Map)
4. Add boundary of region of interest (roi) in to Map
5. Define a function to mask clouds for Landsat 4, 5, 7 and 8
6. Import Landsat image collection based on target year by filtering the date, and roi
7. Mask the clouds of the imported image and clip the image within roi
8. 


cloudMask script is available at (though need to convert to Python Script): https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LE07_C01_T1_SR



```yaml
tagline: "This is a custom tagline content which overrides the default page excerpt."
header:
  overlay_image: /assets/images/unsplash-image-1.jpg
  caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
```