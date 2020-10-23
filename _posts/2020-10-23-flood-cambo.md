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
# gallery1:
#   - url: /images/forest-cambo/FC-2000.jpg
#     image_path: /images/forest-cambo/FC-2000.jpg
#     alt: "Forest Cover in 2000"
#     title: "Figure 2a: Forest Cover in 2000."
#   - url: /images/forest-cambo/FC-2019.jpg
#     image_path: /images/forest-cambo/FC-2019.jpg
#     alt: "Forest Cover in 2019"
#     title: "Figure 2b: Forest Cover in 2019."
# gallery2:
#   - url: /images/forest-cambo/FCL-Cambo.jpg
#     image_path: /images/forest-cambo/FCL-Cambo.jpg
#     alt: "FCL-Cambo"
#     title: "Figure 3a: Forest Cover Loss in Cambodia, 2000-2019."
#   - url: /images/forest-cambo/FCL-TonleSap.jpg
#     image_path: /images/forest-cambo/FCL-TonleSap.jpg
#     alt: "FCL-TonleSap"
#     title: "Figure 3b: Forest Cover Loss in Tonle Sap Area, 2000-2019."
#   - url: /images/forest-cambo/FCL-TechoSen.jpg
#     image_path: /images/forest-cambo/FCL-TechoSen.jpg
#     alt: "FCL-TechoSen"
#     title: "Figure 3c: Forest Cover Loss in Techo Sen Reussey Treb Park, 2000-2019."
#   - url: /images/forest-cambo/FCL-KhnangPsa.jpg
#     image_path: /images/forest-cambo/FCL-KhnangPsa.jpg
#     alt: "FCL-KhnangPsa"
#     title: "Figure 3d: Forest Cover Loss in Khnang Psa Mountain, 2000-2019."
# gallery3:
#   - url: /images/forest-cambo/gain.jpg
#     image_path: /images/forest-cambo/gain.jpg
#     alt: "gain"
#     title: "Figure 4a: Forest Gain in Cambodia, 2000-2012."
#   - url: /images/forest-cambo/gain_neTSL.jpg
#     image_path: /images/forest-cambo/gain_neTSL.jpg
#     alt: "gain_neTSL"
#     title: "Figure 4b: Forest Gain in Northeastern Tonle Sap Lake area, 2000-2012."
# gallery4:
#   - url: /images/forest-cambo/yearlyforest.jpg
#     image_path: /images/forest-cambo/yearlyforest.jpg
#     alt: "yearly-forest"
#     title: "Figure 5: Yearly Forest Cover and Loss Estimation."
---

Heavy rain lashed Cambodia for over a week in October 2020, flooding 18 provinces and Phnom Pench city. According to figures reported by National Committee for Disaster Management in Cambodia from 1st to 19th October, 25 people were reported dead in the floods, about 300,000 people or 78,000 families were affected, and about 37,000 people or 9,000 families were displaced to safer zones. In addition, flood has also destroyed 56 houses and affected over 73,000 houses, while 568 schools were inundated. In this flood event, at least 80,000 ha crops and 210,0000 ha paddy fields were inundated, whereas theirs damages has not been so far reported. On the other hand, many national and provincial roads were severely impacted by the effects of this prolonged flood.
{: style="text-align: justify;"}

{% include gallery caption="Figure 1: Report and data summary on flood impact in 2020 in Cambodia." %}

Even though various data were collected and described in Figure 1 by NCDM, the area of flooding which shows the extend and location of flooding has remained unofficially published by any related institutions. Therefore, I would like to reveal a quick method to detect and extract the inundated area based on Sentinel-1 SAR GRD images by using Google Earth Engine in QGIS application.


Source code is available at: [GitHub](https://github.com/menvuthy/Code_Collection.git)