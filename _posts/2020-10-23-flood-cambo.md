---
classes: wide
title: "Sentinel-1 SAR: Cambodia Flood in October 2020"
tagline: "This is a quick way to detect and extract the inundation area for analysis based on the Sentinel-1 SAR GRD images by using Google Earth Engine in QGIS."
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
last_modified_at: 2020-10-23
gallery:
  - url: /images/flood-cambo/report-1.jpg
    image_path: /images/flood-cambo/report-1.jpg
    alt: "report-data-flood"
    title: "Figure 1a: Report of flood impact in 2020."
  - url: /images/flood-cambo/report-2.jpg
    image_path: /images/flood-cambo/report-2.jpg
    alt: "data-table-flood"
    title: "Figure 1b: Data table of flood impact in 2020 by sector."
  - url: /images/flood-cambo/report-3.jpg
    image_path: /images/flood-cambo/report-3.jpg
    alt: "casaulties-table"
    title: "Figure 1b: Data table of casaulties caused by flood in 2020."
gallery1:
  - url: /images/flood-cambo/Inundation Area_VV.jpg
    image_path: /images/flood-cambo/Inundation Area_VV.jpg
    alt: "Sentinel-1 SAR Image"
    title: "Figure 2a: Sentinel-1 SAR Image of Cambodia from 15-20 October 2020."
gallery2:
  - url: /images/flood-cambo/Inundation Area_VV_Flood.jpg
    image_path: /images/flood-cambo/Inundation Area_VV_Flood.jpg
    alt: "detected-water"
    title: "Figure 2b: Detected flooding area."
  - url: /images/flood-cambo/Inundation Area.jpg
    image_path: /images/flood-cambo/Inundation Area.jpg
    alt: "extracted-water"
    title: "Figure 2c: Extracted flooding area."
Phnompenh:
  - url: /images/flood-cambo/Phnom Penh_VV.jpg
    image_path: /images/flood-cambo/Phnom Penh_VV.jpg
    alt: "sentinel-1-sar-image"
    title: "Figure 3a: Image of Sentinel-1 SAR in Phnom Penh."
  - url: /images/flood-cambo/Phnom Penh.jpg
    image_path: /images/flood-cambo/Phnom Penh.jpg
    alt: "detected-water"
    title: "Figure 3b: Detected flooding area in Phnom Penh."
Siemreap:
  - url: /images/flood-cambo/Siem Reap_VV.jpg
    image_path: /images/flood-cambo/Siem Reap_VV.jpg
    alt: "sentinel-1-sar-image"
    title: "Figure 4a: Image of Sentinel-1 SAR in Siem Reap."
  - url: /images/flood-cambo/Siem Reap.jpg
    image_path: /images/flood-cambo/Siem Reap.jpg
    alt: "detected-water"
    title: "Figure 4b: Detected flooding area in Siem Reap."
Banteaymeanchey:
  - url: /images/flood-cambo/Banteay Meanchey_VV.jpg
    image_path: /images/flood-cambo/Banteay Meanchey_VV.jpg
    alt: "sentinel-1-sar-image"
    title: "Figure 5a: Image of Sentinel-1 SAR in Banteay Meanchey."
  - url: /images/flood-cambo/Banteay Meanchey.jpg
    image_path: /images/flood-cambo/Banteay Meanchey.jpg
    alt: "detected-water"
    title: "Figure 5b: Detected flooding area in Banteay Meanchey."
Battambang:
  - url: /images/flood-cambo/Battambang_VV.jpg
    image_path: /images/flood-cambo/Battambang_VV.jpg
    alt: "sentinel-1-sar-image"
    title: "Figure 6a: Image of Sentinel-1 SAR in Battambang."
  - url: /images/flood-cambo/Battambang.jpg
    image_path: /images/flood-cambo/Battambang.jpg
    alt: "detected-water"
    title: "Figure 6b: Detected flooding area in Battambang."
Pursat:
  - url: /images/flood-cambo/Pursat.jpg
    image_path: /images/flood-cambo/Pursat.jpg
    alt: "sentinel-1-sar-image"
    title: "Figure 7a: Image of Sentinel-1 SAR in Pursat."
  - url: /images/flood-cambo/Pursat.jpg
    image_path: /images/flood-cambo/Pursat.jpg
    alt: "detected-water"
    title: "Figure 7b: Detected flooding area in Pursat."
---

Heavy rain lashed Cambodia for over two weeks in October 2020, flooding 18 provinces and Phnom Pench city. According to figures reported by National Committee for Disaster Management in Cambodia from 1st to 19th October, 25 people were reported dead in the floods, about 300,000 people or 78,000 families were affected, and about 37,000 people or 9,000 families were displaced to safer zones. In addition, flood has also destroyed 56 houses and affected over 73,000 houses, while 568 schools were inundated. In this flood event, at least 80,000 ha crops and 210,000 ha paddy fields were inundated, whereas theirs damages has not been so far reported. On the other hand, many national and provincial roads were severely impacted by the effects of this prolonged flood.
{: style="text-align: justify;"}

{% include gallery caption="Figure 1: Report and data summary on flood impact in 2020 in Cambodia." %}

Even though various data were collected and described in Figure 1 by NCDM, the area of flooding which shows the extend and location of flooding has remained unofficially published by any related institutions. Therefore, I would like to reveal a quick method to detect and extract the inundated area based on Sentinel-1 SAR GRD images by using Google Earth Engine in QGIS application.
{: style="text-align: justify;"}

## Overview of Inundation Area in Cambodia

{% include gallery id="gallery1" %}
{% include gallery id="gallery2" caption="Figure 2: (a) Sentinel-1 SAR Image of Cambodia from 15-20 October 2020. (b) Detected flooding area. (c) Extracted flooding area." %}

## Overview of Inundation Area by City and Provinces

### Phnom Penh City
{% include gallery id="Phnompenh" caption="Figure 3: Image of Sentinel-1 SAR and detected flooding area in Phnom Penh." %}

### Siem Reap
{% include gallery id="Siemreap" caption="Figure 4: Image of Sentinel-1 SAR and detected flooding area in Siem Reap." %}

### Banteay Meanchey
{% include gallery id="Banteaymeanchey" caption="Figure 5: Image of Sentinel-1 SAR and detected flooding area in Banteay Meanchey." %}

### Battambang
{% include gallery id="Battambang" caption="Figure 6: Image of Sentinel-1 SAR and detected flooding area in Battambang." %}

### Pursat
{% include gallery id="Pursat" caption="Figure 7: Image of Sentinel-1 SAR and detected flooding area in Pursat." %}

Source code is available at: [GitHub](https://github.com/menvuthy/Code_Collection.git)