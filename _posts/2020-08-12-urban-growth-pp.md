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

# Landsat Processing Methods

The development of image for each year was performed in Jupiter Notebook without having to download any image collection from the satellite's website and resort to any GIS Desktop software. The entire geoprocessing and remote sensing routine requires `Earth Engine Python API` and `geemap`. The geemap Python package is built upon the `ipyleaflet` and `folium` packages and implements several methods for interacting with Earth Engine data layers, such as `Map.addLayer()`, `Map.setCenter()`, and `Map.centerObject()`. After installation of these packages into your library based on the guidline in `https://geemap.readthedocs.io/en/latest/`, you may follow the main steps below to develop the image:
1. Import `geemap package` into Python
2. Create an interactive map (Map)
3. Add boundary of region of interest (roi) in to Map
4. Define a function to mask clouds for Landsat 4, 5, 7 and 8
5. Import Landsat image collection based on target year by filtering the date, and roi
6. Mask the clouds of the imported image and clip the image within roi
7. Add layer of each image following the target year into Map. For viewing, selection of Bands is different following to the type of Landsat Image.
8. After receiving the cloudMasked images of each year, composite them into a timelapse imagery in a GIF format or a video based on own's interest. 

# Sample Scripts

**1. Import** `geemap package` **into Python**
```yaml
---
# Installs geemap package
import subprocess
try:
    import geemap
except ImportError:
    print('geemap package not installed. Installing ...')
    subprocess.check_call(["python", '-m', 'pip', 'install', 'geemap'])
# Checks whether this notebook is running on Google Colab
try:
    import google.colab
    import geemap.eefolium as geemap
except:
    import geemap
# Authenticates and initializes Earth Engine
import ee
try:
    ee.Initialize()
except Exception as e:
    ee.Authenticate()
    ee.Initialize()  
---
```

**2. Create an interactive map (Map)**
```yaml
---
# Map zooming at Phnom Penh city
Map = geemap.Map(zoom=4)
Map.setCenter(104.8997174646636, 11.555294803579315, 11);
Map
---
```

**3. Add boundary of region of interest (roi) in to Map**

In this project, I used shapefile of Phnom Penh boundary as my region of interest.
```yaml
---
roi = geemap.shp_to_ee('~/PhnomPenh.shp')
Map.addLayer(roi, {}, 'PhnomPenh_Boundary')
---
```







cloudMask script is available at (though need to convert to Python Script): https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LE07_C01_T1_SR
