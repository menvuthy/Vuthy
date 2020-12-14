---
classes: wide
title: "Cambodia: Assessment of Flood Damage on Early, Medium and Late Maturity Rice Crop"
tagline: "My research iPoster for AGU Fall Meeting Conference, Online Everywhere 1-17 December 2020."
header:
  overlay_image: /images/flood-cambo/Homepage.jpg
  teaser: /images/flood-cambo/Homepage.jpg
categories:
  - Flood
tags:
  - Cambodia
  - Flood
  - QGIS
  - Python
  - Earth Engine API
last_modified_at: 2020-12-14
gallery:
  - url: /images/assess-flood-damage/rice-categories.png
    image_path: /images/assess-flood-damage/rice-categories.png
    alt: "rice-categories"
    title: "Figure 1: Growth duration and growth stage of early, medium and late rice crops by phase [1]."
gallery1:
  - url: /images/assess-flood-damage/study-area.png
    image_path: /images/assess-flood-damage/study-area.png
    alt: "study-area"
    title: "Figure 2: Location of study area and annual rice production in Pursat Province."
gallery2:
  - url: /images/assess-flood-damage/survey-loc.png
    image_path: /images/assess-flood-damage/survey-loc.png
    alt: "survey-loc"
    title: "Figure 3: Location of village centers where field survey was conducted."
gallery3:
  - url: /images/assess-flood-damage/survey-farmer.png
    image_path: /images/assess-flood-damage/survey-farmer.png
    alt: "survey-acti"
    title: "Figure 4: Field survey activities with local farmers in the flood affected area in Pursat Province."    
gallery4:
  - url: /images/assess-flood-damage/diagram.png
    image_path: /images/assess-flood-damage/diagram.png
    alt: "diagram"
    title: "Figure 5: Research flowchart."
gallery5:
  - url: /images/assess-flood-damage/simulaiton result.png
    image_path: /images/assess-flood-damage/simulaiton result.png
    alt: "obs-sim-flood"
    title: "Figure 6a: Comparison between observed and simulated discharge of 2011 Flood simulated in RRI model."
  - url: /images/assess-flood-damage/flood-2011.png
    image_path: /images/assess-flood-damage/flood-2011.png
    alt: "obs-sim-flood"
    title: "Figure 6b: Flooding area and depth of 2011 flood simulated in RRI model."
gallery6:
  - url: /images/assess-flood-damage/3-fdcs.png
    image_path: /images/assess-flood-damage/3-fdcs.png
    alt: "3-fdcs"
    title: "Figure 7: Flood depth-duration damage curves for early, medium and late rice crop."
gallery7:
  - url: /images/assess-flood-damage/cost-production rate.png
    image_path: /images/assess-flood-damage/cost-production rate.png
    alt: "cost-production-rate"
    title: "Figure 8: Rice production rate and farm gate price of each rice crop type."
gallery8:
  - url: /images/assess-flood-damage/classification-process.png
    image_path: /images/assess-flood-damage/classification-process.png
    alt: "classification-process"
    title: "Figure 9: NDVI time series of early, medium and late rice crops from MODIS satellite data (left), diagram of paddy area classification method (right)."
gallery9:
  - url: /images/assess-flood-damage/paddy-map.png
    image_path: /images/assess-flood-damage/paddy-map.png
    alt: "paddy-map"
    title: "Figure 10: Paddy area map in 2019 and flood-affected paddy area map in 2011."
---
## I. Introduction
Rice crops are mainly categorized into early, medium and late variety, and they are differently damaged by flood depending on its growth characteristic, productivity, and value.
{: style="text-align: justify;"}

{% include gallery caption="Figure 1: Growth duration and growth stage of early, medium and late rice crops by phase [1]." %}

However, the estimation method of flood damage based on rice crop types remains unexamined in previous studies due to the shortage of past damage data and intensive field survey with local farmers, especially with those who experienced the past flood events. 
{: style="text-align: justify;"}

Hence, this study attempts to:
1. develop the assessment methodology to estimate the flood damage on early, medium and late rice crops based on flood depth and flood duration through development of:
{: style="text-align: justify;"}

* Three Types of Flood Depth-duration and damage Curves (3-Type FDCs) according to field survey with farmers in the flood-affected area.
{: style="text-align: justify;"}
* paddy area map of early, medium and late rice crop by using MODIS satellite imagery.
{: style="text-align: justify;"}

2. Assess the flood damage on rice crops under the past and the present cropping patterns and analyze the impact of different flood frequencies.
{: style="text-align: justify;"}

3. Assess the flood damage on rice crops under the present climate (1979-2003) and future climate (2075-2099) conditions, based on MRI-AGCM3.2S precipitation datasets from previous study [2].
{: style="text-align: justify;"}


This study enriches more understanding on how early, medium and late rice crops are damaged by floodwater with the function of flood depth and flood duration. The assessment method can be applied in other areas; mainly, in the area with scarce data. It also provides essential information about the areas of risk which can be useful for future development activities; particularly, for establishing a flood mitigation policy and strategy for climate change adaptation.
{: style="text-align: justify;"}

-----
## II. Study area and field survey

**1. Study Area**

Pursat province is located at the Southwest of Tonle Sap Lake in Cambodia. It is known as one of the most vulnerable provinces to flood disasters in the country.
{: style="text-align: justify;"}
{% include gallery id="gallery1" caption="Figure 2: Location of study area and annual rice production in Pursat Province." %}

**2. Field Survey**

Target locations: villages which are located in the flood plain areas and in each districts.
{: style="text-align: justify;"}
{% include gallery id="gallery2" caption="Figure 3: Location of study area and annual rice production in Pursat Province." %}

Target farmers: those who had experienced the rice crop damages caused by flood disasters. Flood depth and duration in their rice fields, and damage of their rice production were focused.
{: style="text-align: justify;"}
{% include gallery id="gallery3" caption="Figure 4: Field survey activities with local farmers in the flood affected area in Pursat Province." %}

## III. Methodology

Figure 5 shows the conceptual framework of this study.
{: style="text-align: justify;"}
{% include gallery id="gallery4" caption="Figure 5: Research flowchart." %}

**1. Flood Simulation**

The simulation of flood events including 2011 flood (Figure 6a & 6b), 2-y to 200-y return period floods, and floods under present and future climate were conducted using Rainfall-Runoff Inundation (RRI) model [3].
{: style="text-align: justify;"}
{% include gallery id="gallery5" caption="Figure 6: a) Comparison between observed and simulated discharge of 2011 Flood simulated in RRI model. b) Flooding area and depth of 2011 flood simulated in RRI model." %}

**2. Development of 3-Types FDCs**

The data collected from field survey with 95 local farmers were used to develop flood depth-duration damage curves (Figure 7) and also to determine the rice production rate and farm gate price for damage cost calculation (Figure 8).
{: style="text-align: justify;"}
{% include gallery id="gallery6" caption="Figure 7: Flood depth-duration damage curves for early, medium and late rice crop." %}

{% include gallery id="gallery7" caption="Figure 8: Rice production rate and farm gate price of each rice crop type." %}

**3. Development of Paddy Area Map**

Based on the report from local government which indicates the location of early, medium and late paddy areas, the characteristics of NDVI time series for each type of rice were observed from MODIS Satellite Data (Figure 9. left). From this observation, the method to classify the paddy areas for early, medium and late rice crops were determined (Figure 9. right).
{: style="text-align: justify;"}

{% include gallery id="gallery8" caption="Figure 9: NDVI time series of early, medium and late rice crops from MODIS satellite data (left), diagram of paddy area classification method (right)." %}

By following the above classification method, the paddy area map in 2019 (present cropping pattern) and flood-affected paddy area map in 2011 (past cropping pattern) were developed.
{: style="text-align: justify;"}

{% include gallery id="gallery9" caption="Figure 10: Paddy area map in 2019 and flood-affected paddy area map in 2011." %}

## Methodology

Visualizing the Sentinel-1 SAR images, dectecting waterbody, and extracting it for other analysis can be performed in Google Earth Engine and QGIS by using EE Python API. Therefore, it is important to equip with some background on programming language and QGIS application. Below, I will instruct a few steps on how to visualize the images, detect waterbody and extract inundation area for other computation and analysis.
{: style="text-align: justify;"}

**1. Visualizing the Sentinel-1 SAR GRD images**

The platform to run the script is [CodeGEE](https://code.earthengine.google.com). Filter the collection of Sentinel-1 SAR GRU images for the VV and VH product from the descending track. Filter the date of interest, and add image layer into the map by clipping only Cambodia boundary. Here I used only VV products to analyze the waterbody. VH product can also be used; however, threshold value for determining the waterbody may be slightly different from VH product.
{: style="text-align: justify;"}

```yaml
---
// Load country features from Large Scale International Boundary (LSIB) dataset.
var countries = ee.FeatureCollection('USDOS/LSIB_SIMPLE/2017');
var roi = countries.filter(ee.Filter.eq('country_co', 'CB'));
Map.addLayer(roi,{},'Cambodia')

//Let's centre the map view over our ROI
Map.centerObject(roi, 6);

// Filter the collection for the VV product from the descending track
var collectionVV = ee.ImageCollection('COPERNICUS/S1_GRD')
    .filter(ee.Filter.eq('instrumentMode', 'IW'))
    .filter(ee.Filter.listContains('transmitterReceiverPolarisation', 'VV'))
    .filter(ee.Filter.eq('orbitProperties_pass', 'DESCENDING'))
    .filterBounds(roi)
    .select(['VV'])
    .median();

// Filter the collection for the VH product from the descending track
var collectionVH = ee.ImageCollection('COPERNICUS/S1_GRD')
    .filter(ee.Filter.eq('instrumentMode', 'IW'))
    .filter(ee.Filter.listContains('transmitterReceiverPolarisation', 'VH'))
    .filter(ee.Filter.eq('orbitProperties_pass', 'DESCENDING'))
    .filterBounds(roi)
    .select(['VH'])
    .median();

// Adding the VV layer to the map at a specific date
var image = ee.Image(collectionVV.filterDate('2020-10-14', '2020-10-20').median());
Map.addLayer(image.clip(roi), {min: -25, max: 5}, 'Image_VV');
---
```

**2. Detecting inundation area**

The threshold value to differentiate the waterbody from the image is determined from the value of frequency value of VV. The value in the first peak area are generally considered as water value, while other high frequency value represents other types of classification including building, road, bared soil, crops, and forest. In order to compute, the scale should be set based on the size of the region of interest. The smaller the ROI is, the smaller the scale is. In the Cambodia scale, 500 resolution is set due to the fact that the higher resolution might not work due to the limition in GEE cloud when it comes to exporting.
{: style="text-align: justify;"}

```yaml
---
// Compute the histogram of the Image
var histogram = image.reduceRegion({
  reducer: ee.Reducer.histogram(255, 2)
      .combine('mean', null, true)
      .combine('variance', null, true), 
  geometry: roi, 
  scale: 500,
  bestEffort: true
});

// Chart the histogram
print(Chart.image.histogram(image, roi, 500));
---
```
{% include gallery id="gallery3" caption="Figure 15: Histogram of VV showing the value for different type of landuse." %}

**3. Extract and export the image of inundation area**

The image pixels are classified as waterbody where theirs VV values are less than the threshold defined in Step 2, and the classified area can be extracted by masking the non-water area and clipped for Cambodia boundary. The classified image can be then exported as GeoTIFF by setting high maxPixels following the size of the region of interest. By running the code below in GEE, the result of inundation area as GeoTIFF file will be stored in the Google drive.
{: style="text-align: justify;"}

**Notice:** The smaller scale, the higher maxPixels.
{: .notice--success}

```yaml
---
// Chart the histogram
print(Chart.image.histogram(image, roi, 500));

// Classify the Image
var flood = image.lt(-15);
Map.addLayer(flood.mask(flood).clip(roi), {palette: 'blue'}, 'Flood');

Export.image.toDrive({
  image: flood.mask(flood).clip(roi),
  description: 'FloodMap_2',
  scale: 10,
  region: roi,
  maxPixels:4000000000000
});
---
```

**Notice:** In order to achieve similar result in QGIS, the script described above shall be converted into EE Python API.
{: .notice--success}

-----
## Comment

I hope this instruction can be useful for engineering student or young professional who may need this lesson to work on their project. For the whole workflow, you may contact me directly. If you have any questions or suggestions, please feel free to let me know.
{: style="text-align: justify;"}

Thank you!

**Related websites**
1. [Code Platform of Google Earth Engine](https://code.earthengine.google.com)

-----

Source code is available at: [GitHub](https://github.com/menvuthy/Code_Collection.git)