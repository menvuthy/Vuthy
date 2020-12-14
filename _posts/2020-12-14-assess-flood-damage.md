---
classes: wide
title: "Cambodia: Assessment of Flood Damage on Early, Medium and Late Maturity Rice Crop"
tagline: "iPoster of my research for American Geophysical Union Fall Meeting, Online Everywhere 1-17 December 2020.."
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
gallery10:
  - url: /images/assess-flood-damage/dm-result-validation.png
    image_path: /images/assess-flood-damage/dm-result-validation.png
    alt: "dm-result-validation"
    title: "Table 1: Result summary of rice crop damage estimated by 3-Type FDCs and by MRC FDC, compared with reported damage."
gallery11:
  - url: /images/assess-flood-damage/dm-cpt.png
    image_path: /images/assess-flood-damage/dm-cpt.png
    alt: "dm-cpt"
    title: "Figure 11: Result summary of rice crop damage under the past and the present cropping patterns from 2-y to 200-y return period floods."    
gallery12:
  - url: /images/assess-flood-damage/dm-clm.png
    image_path: /images/assess-flood-damage/dm-clm.png
    alt: "dm-clm"
    title: "Figure 12: Flood damage on early, medium and late rice crop under climate change impact."  
gallery13:
  - url: /images/assess-flood-damage/dm-clm-map.png
    image_path: /images/assess-flood-damage/dm-clm-map.png
    alt: "dm-clm-map"
    title: "Figure 13: Map of damaged paddy area under the impact of climate change"
gallery14:
  - url: /images/assess-flood-damage/dm-clm-map.png
    image_path: /images/assess-flood-damage/dm-clm-map.png
    alt: "dm-clm-map"
    title: "Figure 13: Map of damaged paddy area under the impact of climate change"
gallery14:
  - url: /images/assess-flood-damage/agu-interface.png
    image_path: /images/assess-flood-damage/agu-interface.png
    alt: "agu-interface"
    title: "Website interface of AGU Fall Meeting"
  - url: /images/assess-flood-damage/iposter.png
    image_path: /images/assess-flood-damage/iposter.png
    alt: "iposter"
    title: "Overview of iPoster"
---
## Overview of iPoster at AGU Fall Meeting conference
{% include gallery id="gallery14" %}

## Introduction
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

2. Assess the flood damage on rice crops under the past and the present cropping patterns and analyze the impact of different flood frequencies.
{: style="text-align: justify;"}
3. Assess the flood damage on rice crops under the present climate (1979-2003) and future climate (2075-2099) conditions, based on MRI-AGCM3.2S precipitation datasets from previous study [2].
{: style="text-align: justify;"}


This study enriches more understanding on how early, medium and late rice crops are damaged by floodwater with the function of flood depth and flood duration. The assessment method can be applied in other areas; mainly, in the area with scarce data. It also provides essential information about the areas of risk which can be useful for future development activities; particularly, for establishing a flood mitigation policy and strategy for climate change adaptation.
{: style="text-align: justify;"}

-----
## Study area and field survey

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
{% include gallery id="gallery3" caption="Figure 4: Field survey activities with local farmers in the flood affected area in Pursat Province." %} -->

-----
## Methodology

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

-----
## Flood damage assessment

**1. Validation of Assessment Method**

The flood damages were assessed based on flood simulation, paddy area map, and 3-Type FDCs. The results were compared with the damage estimated by using previous method (Table 1). 
{: style="text-align: justify;"}
{% include gallery id="gallery10" caption="Table 1: Result summary of rice crop damage estimated by 3-Type FDCs and by MRC FDC, compared with reported damage." %}

* The total damage of rice crop estimated by 3-Type FDCs well agreed with the reported damage.
{: style="text-align: justify;"}
* The newly developed method could assess the damage based on rice type, while it is unable with the conventional MRC method.
{: style="text-align: justify;"}

**2. Assessment under Past and Present Cropping Pattern**

Under the flood magnitude of various return period, the rice crop damage on past and present cropping patterns were assessed based on 3-Type FDCs.
{: style="text-align: justify;"}

{% include gallery id="gallery11" caption="Figure 11: Result summary of rice crop damage under the past and the present cropping patterns from 2-y to 200-y return period floods." %}

* Damage area and damage cost of present cropping pattern were overall greater than the past. It also increases following the larger flood magnitudes.
{: style="text-align: justify;"}
* Under present cropping pattern, the damage is mainly attributed to Early rice crop, while in the past cropping pattern, the main contribution is from Late rice crop.
{: style="text-align: justify;"}
* First, it is because the area of rice cultivation expanded significantly in the present pattern. Last is because early rice has high price and production rate compared to others, so the more early rice is grown, the more damage comes from early rice.
{: style="text-align: justify;"}

Therefore, present cropping pattern requires higher budget for saving rice production chain after flooding. This information can be used for long-term cost-benefit analysis.
{: style="text-align: justify;"}

**3. Assessment under Present and Future Climate**

Based on MRI-AGCM3.2S precipitation datasets from previous study [2], the damage under the past and future climate were assessed (Figure12).
{: style="text-align: justify;"}

{% include gallery id="gallery12" caption="Figure 12: Flood damage on early, medium and late rice crop under climate change impact." %}


* There would be overall growth of rice crop damage in the future climate.
{: style="text-align: justify;"}
* Total damage under future climate would be more than 35,000 ha or 25 million USD = 14% higher than damage under present climate.
{: style="text-align: justify;"}

{% include gallery id="gallery13" caption="Figure 13: Map of damaged paddy area under the impact of climate change." %}

* Bakan and Kandieng district are the most affected and damaged area in the future climate condition since they have more rice fields compared to others.
{: style="text-align: justify;"}

-----
## Conclusion and acknowledgement

**Summary**

* Flood Depth-duration damage Curves (3-Type FDCs) for Early, Medium and Late rice crop were developed and showed more advantages over previous assessment methods.
* Comparison of cropping patterns, and analysis of climate change impact were studied.
* Method for creating Paddy Area Map based on MODIS satellite image was developed.

**Impact**

* This study enriches more understanding on how early, medium and late rice crops are affected by floodwater with the function of flood depth and flood duration.
* The developed method can be applicable in other areas; particularly, in area with scarce data.
* This study also provides an essential information about the areas of risk based on flood damage estimation and the impact of climate change on all types of rice crop
* It can be useful for future development activities; in particular, when it comes to establishing a flood mitigation policy for the sake of disaster risk reduction and implementing the flood mitigation actions for climate change adaptation. 

**Acknowledgement**

This research was financially supported by Japanese Government (MEXT) Scholarship Program, educational support and guidance from River and Environmental Engineering Laboratory at The University of Tokyo. Furthermore, the field investigation was supported by JSPS KAKENHI Grant Number 18H03823 and the Water Cycle Data Integrator, Academic-Industry Collaboration Program, The University of Tokyo. The author also would like to highly appreciate all persons concerned and Cambodian government officers who helped facilitate towards the completion of this study.

-----
## Reference
[1]  IRRI, “Crop calendar,” tech. rep., International Rice Research Institute.

[2] B.B.Shrestha,E.D.P.Perera,S.Kudo,M.Miyamoto,Y.Yamazaki,D.Kuribayashi, H. Sawano, T. Sayama, J. Magome, A. Hasegawa, et al., “Assessing flood disaster impacts in agriculture under climate change in the river basins of southeast asia,” Natural Hazards, vol. 97, no. 1, pp. 157–192, 2019.

[3] T. Sayama, G. Ozawa, T. Kawakami, S. Nabesaka, and K. Fukami, “Rainfall– runoff–inundation analysis of the 2010 pakistan flood in the kabul river basin,” Hydrological Sciences Journal, vol. 57, no. 2, pp. 298–312, 2012.