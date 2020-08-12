---
title: "Phnom Penh: Urban Growth from 1988 to 2020 by Landsat Satellite Imagery"
tagline: "This timelapse image reveals 33-year growth of Phnom Penh city."
header:
  overlay_image: /images/pp-growth/head-image.png
  caption: "Photo credit: [**Photopea**](https://photopea.com)"
tags:
  - table of contents
toc: true
toc_label: "Content"
toc_icon: "cog"
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

The development of image for each year was performed in Jupiter Notebook without having to download any image collection from the satellite's website and resort to any GIS Desktop software. The entire geoprocessing and remote sensing routine requires `Earth Engine Python API` and `geemap`. The geemap Python package is built upon the `ipyleaflet` and `folium` packages and implements several methods for interacting with Earth Engine data layers, such as `Map.addLayer()`, `Map.setCenter()`, and `Map.centerObject()`. 

After installation of these packages into your library based on the guideline of [geemap](https://geemap.readthedocs.io/en/latest/), you may follow the main steps below to develop the image:
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

**4. Define a function to mask clouds for Landsat 4, 5, 7 and 8**

CloudMask script is available at [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LE07_C01_T1_SR); however, converting from Java scripts to Python scripts is necessary. 
```yaml
---
# Surface reflectance QA band to mask clouds.
def cloudMaskL457(image):
  qa = image.select('pixel_qa')
  # If the cloud bit (5) is set and the cloud confidence (7) is high
  # or the cloud shadow bit is set (3), then it's a bad pixel.
  cloud = qa.bitwiseAnd(1 << 5) \
          .And(qa.bitwiseAnd(1 << 7)) \
          .Or(qa.bitwiseAnd(1 << 3))
# Remove edge pixels that don't occur in all bands
  mask2 = image.mask().reduce(ee.Reducer.min())
  return image.updateMask(cloud.Not()).updateMask(mask2)
---
```
**5. Import Landsat image collection based on target year**

The Landsat satellite images are followed by the year. For instance, Lansat 5 is 1984-2012, Landsat 7 is 1999-present, and Landsat 8 is 2013-present. Further details about each Landsat satellite image is described [Here](https://developers.google.com/earth-engine/datasets/catalog/landsat). Therefore, the earlier years can also be found in the image collection of old satellite, too.

```yaml
---
# Landsat 5, Year: 2000
collection_2000 = ee.ImageCollection('LANDSAT/LT05/C01/T1_SR') \
    .filterDate('2000-01-01', '2000-12-31')\
    .filterBounds(roi)

PP_2000 = collection_2000 \
    .map(cloudMaskL457) \
    .median()\
    .clip(roi)

# Landsat 7, Year: 2010
collection_2010 = ee.ImageCollection('LANDSAT/LE07/C01/T1_SR') \
    .filterDate('2010-01-01', '2010-12-31')\
    .filterBounds(roi)

PP_2010 = collection_2010 \
    .map(cloudMaskL457) \
    .median()\
    .clip(roi)

# Landsat 8, Year: 2020
collection_2020 = ee.ImageCollection('LANDSAT/LC08/C01/T1_SR') \
    .filterDate('2020-01-01', '2020-08-05')\
    .filterBounds(roi)

PP_2020 = collection_2020 \
    .map(cloudMaskL457) \
    .median()\
    .clip(roi)
---
```

**6. Mask the clouds of the imported image and clip the image within roi**

```yaml
---
# Mask cloud of image in 2000
PP_2000 = collection_2000 \
    .map(cloudMaskL457) \
    .median()\
    .clip(roi)

# Mask cloud of image in 2010
PP_2010 = collection_2010 \
    .map(cloudMaskL457) \
    .median()\
    .clip(roi)

# Mask cloud of image in 2020
PP_2020 = collection_2020 \
    .map(cloudMaskL457) \
    .median()\
    .clip(roi)
---
```