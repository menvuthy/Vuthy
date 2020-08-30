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
    title: "Figure 1a: Global Forest Cover in 2000."
  - url: /images/forest-cambo/global-forest-loss.jpg
    image_path: /images/forest-cambo/global-forest-loss.jpg
    alt: "global-forest-cover-loss"
    title: "Figure 1b: Global Forest Cover Loss from 2000 to 2019."
gallery1:
  - url: /images/forest-cambo/FC-2000.jpg
    image_path: /images/forest-cambo/FC-2000.jpg
    alt: "Forest Cover in 2000"
    title: "Figure 2a: Forest Cover in 2000."
  - url: /images/forest-cambo/FC-2019.jpg
    image_path: /images/forest-cambo/FC-2019.jpg
    alt: "Forest Cover in 2019"
    title: "Figure 2b: Forest Cover in 2019."
gallery2:
  - url: /images/forest-cambo/FCL-Cambo.jpg
    image_path: /images/forest-cambo/FCL-Cambo.jpg
    alt: "FCL-Cambo"
    title: "Figure 3a: Forest Cover Loss in Cambodia, 2000-2019."
  - url: /images/forest-cambo/FCL-TonleSap.jpg
    image_path: /images/forest-cambo/FCL-TonleSap.jpg
    alt: "FCL-TonleSap"
    title: "Figure 3b: Forest Cover Loss in Tonle Sap Area, 2000-2019."
  - url: /images/forest-cambo/FCL-TechoSen.jpg
    image_path: /images/forest-cambo/FCL-TechoSen.jpg
    alt: "FCL-TechoSen"
    title: "Figure 3c: Forest Cover Loss in Techo Sen Reussey Treb Park, 2000-2019."
  - url: /images/forest-cambo/FCL-KhnangPsa.jpg
    image_path: /images/forest-cambo/FCL-KhnangPsa.jpg
    alt: "FCL-KhnangPsa"
    title: "Figure 3d: Forest Cover Loss in Khnang Psa Mountain, 2000-2019."
gallery3:
  - url: /images/forest-cambo/gain.jpg
    image_path: /images/forest-cambo/gain.jpg
    alt: "gain"
    title: "Figure 4a: Forest Gain in Cambodia, 2000-2012."
  - url: /images/forest-cambo/gain_neTSL.jpg
    image_path: /images/forest-cambo/gain_neTSL.jpg
    alt: "gain_neTSL"
    title: "Figure 4b: Forest Gain in Northeastern Tonle Sap Lake area, 2000-2012."
gallery4:
  - url: /images/forest-cambo/yearlyforest.jpg
    image_path: /images/forest-cambo/yearlyforest.jpg
    alt: "yearly-forest"
    title: "Figure 5: Yearly Forest Cover and Loss Estimation."
---

Forest cover plays an essential role in delivering important ecosystem services, including biodiversity richness, climate regulation, carbon storage, and water supplies (1). However, spatially and temporally detailed information on global-scale forest cover changes at a high resolution did not exist until M.C. Hansen and his team in the University of Maryland, USA developed a global-scale forest change and published the works in 2013 (2). Hansen et al. 2013 (2) mapped global tree cover extent, loss, and gain annually for the period from 2000 to 2012 from Landsat imagery at a spatial resolution of 30 m, especially the datasets have been updated every year. 
{: style="text-align: justify;"}

The data source of information content presented here is publicly availble for both [download](https://earthenginepartners.appspot.com/science-2013-global-forest/download_v1.7.html) and [web-based visualizations](http://earthenginepartners.appspot.com/science-2013-global-forest). However, downloading and processing such a large dataset are extremely tedious, and extracting it for analysis on a cloud platform can be the main challenges for some engineers and scientists who are struggling with remote sensing technology. Therefore, here I will illustrate one of many remote sensing methods to extract the datasets to:
{: style="text-align: justify;"}

1. Visualize the global forest cover in 2000, and forest cover loss during the period 2000-2019. 
2. Examine the spatial and temporal changes of both forest cover loss and gain in Cambodia from 2000 to 2019.
3. Compute the yearly forest loss in Cambodia from 2000 to 2019.
{: style="text-align: justify;"}

**Primary Notice:** These dataset illustration and visualization are aimed for [Education Purpose](#)  only.
{: .notice--success}

## Global Forest Cover and Loss

In this dataset, there are four important definitions as following:
* **Trees** are defined as vegetation taller than 5m in height and are expressed as a percentage per output grid cell.
* **Forest Cover Loss** is defined as a stand-replacement disturbance, or a change from a forest to non-forest state, during the period 2000–2019. 
* **Forest Cover Gain** is defined as the inverse of loss, or a non-forest to forest change entirely within the period 2000–2012. 
* **Forest Loss Year** is a disaggregation of total ‘Forest Loss’ to annual time scales.
{: style="text-align: justify;"}

{% include gallery caption="Figure 1: (a) Global forest cover in 2000. (b) Global forest cover loss from 2000 to 2019." %}


## Forest Cover Loss and Gain in Cambodia

* **Forest Cover Loss**

Figure 2 shows the comparison image of forest cover between 2000 and 2019 of the whole country.

{% include gallery id="gallery1" caption="Figure 2: (a) Forest cover in 2000. (b) Forest cover in 2019." %}

Video showing spatial and temporal changes of forest cover in Cambodia from 2000 to 2019.

<iframe width="1280" height="720" src="https://www.youtube.com/embed/4D_sMds61jY" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
-----

By only viewing the video, the forest cover loss of some areas are exaggerated due to the far view of image and also the low density of forest canopy at those areas; hence, it is important to zoom into some specific areas to have a closer view of the forest cover and loss. Figure 3 are the images of some well-known areas in Cambodia which provide a clearer and closer look on forest cover and loss.
{: style="text-align: justify;"}

{% include gallery id="gallery2" layout="half" caption="Figure 3: Forest cover loss in the period 2000-2019. (a) Cambodia overview. (b) Area around Tonle Sap Lake. (c) Techo Sen Reussey Treb Park. (d) Khnang Psa mountainous area." %}

* **Forest Cover Gain**

Figure 4 shows the image of forest gain between 2000 and 2012 of the whole Cambodia and Northeastern Tonle Sap Lake area.
{: style="text-align: justify;"}

{% include gallery id="gallery3" caption="Figure 4: Forest Gain 2000-2012. (a) Cambodia. (b) Northeastern Tonle Sap Lake area." %}

## Yearly Forest Cover and Loss in Cambodia

Forest loss was defined as a stand-replacement disturbance or the complete removal of tree cover canopy at the Landsat pixel scale (2). The estimation yearly forest cover and loss are shown in figures below (Figure 5):
{: style="text-align: justify;"}

**Warning Notice:** All computed values here are the rough estimation based on the instruction from [Google Earth Engine](https://developers.google.com/earth-engine/tutorials/tutorial_forest_03a). The user should be concerned of the accuracy with the actual data in their region of interest.
{: .notice--danger}
{% include gallery id="gallery4" caption="Figure 5: Yearly forest cover and loss estimated for Cambodia." %}

## Methodology

Extraction, computation and visualization of Hansen et al. 2013 (2) global forest cover data in this work are performed on cloud platform with the help of QGIS, Python, and Google Earth Engine. Therefore, it is important to equip with some background on programming language and QGIS application. Below, I will instruct how to extract, visualize, and compute the global forest cover data, and Cambodia will be chosen as a case study.
{: style="text-align: justify;"}

**1. Extraction and Visualization of Global Forest Cover and Loss**

There are many methods to extract and visulaize the remote sensing dataset, for example, by using Earth Engine JavaScript API. Under this purpose, it is, however, conducted in QGIS since the performace and loading speed of interactive maps are better. In order to connect QGIS with the earth engine datasets, installation of [Google Earth Engine Plugin](https://youtu.be/RNbzhlMHekU) is first necessary. After that, open the Python Console in QGIS, and the global forest cover data will appear by running the script I provide here with the short description written with the hashtag (#) sign.
{: style="text-align: justify;"}

```yaml
---
# Import module
import ee
from ee_plugin import Map

# Add Earth Engine dataset
image = ee.Image('UMD/hansen/global_forest_change_2019_v1_7')
forest = image.select(['treecover2000'])
loss = image.select(['loss'])
lossYear = image.select(['lossyear'])

# visualization setting
vis = {
'min': 0, 
'max': 100, 
'palette': ['#000000', '#005500', '#00AB00', '#00FF00']
}

# Add layer by masking the unecessary pixels from the map
Map.addLayer(forest.updateMask(forest), vis , 'Global Forest in 2000')
Map.addLayer(loss.updateMask(loss), {'palette': ['#FF0000']} , 'Loss 2000-2019')
---
```

**2. Examination of Forest Cover Loss and Gain in Cambodia**

In order to target to any area, the boundary feature must be given so that the dataset will be clipped and shown for that feature only. In this example, Cambodia boundary was extracted from [Large Scale International Boundary](https://developers.google.com/earth-engine/datasets/catalog/USDOS_LSIB_SIMPLE_2017) (LSIB) dataset provided by the United States Office of the Geographer. After setting the boundary of Cambodia, the forest cover loss and gain can be shown by running the script below. Besides QGIS, it can also be done in Google Earth Engine based on the instruction on [Quantifying Forest Change](https://developers.google.com/earth-engine/tutorials/tutorial_forest_03); however, it may be a bit challenging when it comes to downloading the data from cloud to local storage for analyzing or mapping.
{: style="text-align: justify;"}

```yaml
---
import ee
from ee_plugin import Map

countries = ee.FeatureCollection('USDOS/LSIB_SIMPLE/2017')
# // Get a feature collection with just the Cambodia feature.
roi = countries.filter(ee.Filter.eq('country_co', 'CB'))

# Add Landsat 8 Imagery for the year 2000 and 2019
L8_2000 = ee.ImageCollection('LANDSAT/LT05/C01/T1_SR') \
    .filterDate('2000-01-01', '2000-12-31')\
    .filterBounds(roi)
L8_2019 = ee.ImageCollection('LANDSAT/LC08/C01/T1_SR') \
    .filterDate('2019-01-01', '2019-12-31')\
    .filterBounds(roi)

# Define CloudMask Function
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

CB_2000 = L8_2000 \
    .map(cloudMaskL457) \
    .median()\
    .clip(roi)
CB_2019 = L8_2019 \
    .map(cloudMaskL457) \
    .median()\
    .clip(roi)

# visualization setting
vis_1 = {
    'bands': ['B5', 'B4', 'B3'],
    'min': 0,
    'max': 4000,
    'gamma': [1, 1, 1]
}
vis_2 = {
    'bands': ['B6', 'B5', 'B4'],
    'min': 0,
    'max': 4000,
    'gamma': [1, 1, 1]
}

Map.addLayer(CB_2000, vis_1, 'CB_2000')
Map.addLayer(CB_2019, vis_2, 'CB_2019')

# Add Earth Engine dataset
image = ee.Image('UMD/hansen/global_forest_change_2019_v1_7').clip(roi)
treeCover = image.select(['treecover2000'])          
lossImage = image.select(['loss'])
gainImage = image.select(['gain'])

# visualization setting
vis = {
'min': 0, 
'max': 100, 
'palette': ['#000000', '#005500', '#00AB00', '#00FF00']
}

# Add the tree cover layer in green.
Map.addLayer(treeCover.updateMask(treeCover), vis , 'Forest in 2000')

# Add the loss layer in red.
Map.addLayer(lossImage.updateMask(lossImage),{'palette': ['FF0000']}, 'Loss')

# Add the gain layer in blue.
Map.addLayer(gainImage.updateMask(gainImage),{'palette': ['0000FF']}, 'Gain')
---
```

As for creating yearly forest cover map, the following script was written based on the data instruction on [Image Calculation](https://sites.google.com/site/earthengineapidocs/tutorials/global-forest-change-tutorial/basic-image-calculations?authuser=1). Here is the script for creating the images of each year:
{: style="text-align: justify;"}

```yaml
---
import ee
from ee_plugin import Map

countries = ee.FeatureCollection('USDOS/LSIB_SIMPLE/2017')
roi = countries.filter(ee.Filter.eq('country_co', 'CB'))

image = ee.Image('UMD/hansen/global_forest_change_2019_v1_7').clip(roi)
forest = image.select(['treecover2000'])
loss = image.select(['loss'])
lossYear = image.select(['lossyear'])

#2001
lossInFirst1 = lossYear.gte(1).And(lossYear.lte(1))
forestAt2001 = forest.where(lossInFirst1.eq(1), 0)
#2002
lossInFirst2 = lossYear.gte(1).And(lossYear.lte(2))
forestAt2002 = forest.where(lossInFirst2.eq(1), 0)
#2003
lossInFirst3 = lossYear.gte(1).And(lossYear.lte(3))
forestAt2003 = forest.where(lossInFirst3.eq(1), 0)
#2004
lossInFirst4 = lossYear.gte(1).And(lossYear.lte(4))
forestAt2004 = forest.where(lossInFirst4.eq(1), 0)
#2005
lossInFirst5 = lossYear.gte(1).And(lossYear.lte(5))
forestAt2005 = forest.where(lossInFirst5.eq(1), 0)
#2006
lossInFirst6 = lossYear.gte(1).And(lossYear.lte(6))
forestAt2006 = forest.where(lossInFirst6.eq(1), 0)
#2007
lossInFirst7 = lossYear.gte(1).And(lossYear.lte(7))
forestAt2007 = forest.where(lossInFirst7.eq(1), 0)
#2008
lossInFirst8 = lossYear.gte(1).And(lossYear.lte(8))
forestAt2008 = forest.where(lossInFirst8.eq(1), 0)
#2009
lossInFirst9 = lossYear.gte(1).And(lossYear.lte(9))
forestAt2009 = forest.where(lossInFirst9.eq(1), 0)
#2010
lossInFirst10 = lossYear.gte(1).And(lossYear.lte(10))
forestAt2010 = forest.where(lossInFirst10.eq(1), 0)
#2011
lossInFirst11 = lossYear.gte(1).And(lossYear.lte(11))
forestAt2011 = forest.where(lossInFirst11.eq(1), 0)
#2012
lossInFirst12 = lossYear.gte(1).And(lossYear.lte(12))
forestAt2012 = forest.where(lossInFirst12.eq(1), 0)
#2013
lossInFirst13 = lossYear.gte(1).And(lossYear.lte(13))
forestAt2013 = forest.where(lossInFirst13.eq(1), 0)
#2014
lossInFirst14 = lossYear.gte(1).And(lossYear.lte(14))
forestAt2014 = forest.where(lossInFirst14.eq(1), 0)
#2015
lossInFirst15 = lossYear.gte(1).And(lossYear.lte(15))
forestAt2015 = forest.where(lossInFirst15.eq(1), 0)
#2016
lossInFirst16 = lossYear.gte(1).And(lossYear.lte(16))
forestAt2016 = forest.where(lossInFirst16.eq(1), 0)
#2017
lossInFirst17 = lossYear.gte(1).And(lossYear.lte(17))
forestAt2017 = forest.where(lossInFirst17.eq(1), 0)
#2018
lossInFirst18 = lossYear.gte(1).And(lossYear.lte(18))
forestAt2018 = forest.where(lossInFirst18.eq(1), 0)
#2019
lossInFirst19= lossYear.gte(1).And(lossYear.lte(19))
forestAt2019 = forest.where(lossInFirst19.eq(1), 0)

vis = {
'min': 0, 
'max': 100, 
'palette': ['#000000', '#005500', '#00AB00', '#00FF00']
}

Map.addLayer(forestAt2001.updateMask(forestAt2001), vis, 'Forest in 2001')
Map.addLayer(forestAt2002.updateMask(forestAt2002), vis, 'Forest in 2002')
Map.addLayer(forestAt2003.updateMask(forestAt2003), vis, 'Forest in 2003')
Map.addLayer(forestAt2004.updateMask(forestAt2004), vis, 'Forest in 2004')
Map.addLayer(forestAt2005.updateMask(forestAt2005), vis, 'Forest in 2005')
Map.addLayer(forestAt2006.updateMask(forestAt2006), vis, 'Forest in 2006')
Map.addLayer(forestAt2007.updateMask(forestAt2007), vis, 'Forest in 2007')
Map.addLayer(forestAt2008.updateMask(forestAt2008), vis, 'Forest in 2008')
Map.addLayer(forestAt2009.updateMask(forestAt2009), vis, 'Forest in 2009')
Map.addLayer(forestAt2010.updateMask(forestAt2010), vis, 'Forest in 2010')
Map.addLayer(forestAt2011.updateMask(forestAt2011), vis, 'Forest in 2011')
Map.addLayer(forestAt2012.updateMask(forestAt2012), vis, 'Forest in 2012')
Map.addLayer(forestAt2013.updateMask(forestAt2013), vis, 'Forest in 2013')
Map.addLayer(forestAt2014.updateMask(forestAt2014), vis, 'Forest in 2014')
Map.addLayer(forestAt2015.updateMask(forestAt2015), vis, 'Forest in 2015')
Map.addLayer(forestAt2016.updateMask(forestAt2016), vis, 'Forest in 2016')
Map.addLayer(forestAt2017.updateMask(forestAt2017), vis, 'Forest in 2017')
Map.addLayer(forestAt2018.updateMask(forestAt2018), vis, 'Forest in 2018')
Map.addLayer(forestAt2019.updateMask(forestAt2019), vis, 'Forest in 2019')
---
```

**3. Computation of Yearly Forest Loss in Cambodia**

The computation for yearly forest cover and loss are conducted both in [Earth Engine Code Editor](https://code.earthengine.google.com) and Python in Jupiter Notebook. Based on the instruction on how to quantify the yearly forest loss in the [GEE guideline](https://developers.google.com/earth-engine/tutorials/tutorial_forest_03a), the yearly forest loss in Cambodia can be estimated by changing the region of interest of the provided script. Regarding the detail estimation method, please carefully read the guideline of dataset usage.
{: style="text-align: justify;"}


The forest cover area was calculated by summing all forest pixels within the boundary of Cambodia in 2019, while forest cover loss was calculated based on provided script in Google Earth Engine.
{: style="text-align: justify;"}


## Reference
1. Foley, Jonathan A., et al. "Global consequences of land use." science 309.5734 (2005): 570-574.
2. Hansen, Matthew C., et al. "High-resolution global maps of 21st-century forest cover change." science 342.6160 (2013): 850-853.