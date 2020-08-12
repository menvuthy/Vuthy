---
title: "Phnom Penh: Urban Growth from 1988 to 2020 by Landsat Satellite Imagery"
tagline: "This timelapse image reveals 33-year growth of Phnom Penh city."
header:
  overlay_image: /images/pp-growth/head-image.png
  # caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
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
{% capture fig_img %}
![Foo]({{ "/images/pp-collage.jpg" | relative_url }})
{% endcapture %}

<figure>
  {{ fig_img | markdownify | remove: "<p>" | remove: "</p>" }}
  <figcaption>Phnom Penh city in 1988 (population ~615,000) and 2020 (population ~2,080,000). Images: Landsat Satellite</figcaption>
</figure>

More than thirty years ago, buildings and streets were barely on the map of Phnom Penh city. In 1988 it was home to approximately 615,000 people; however, 33 years later that had risen to more than 2 million (Source: worldpopulationreview.com).


This post should display a **header with an overlay image** and **custom tagline**, if the theme supports it.

Non-square images can provide some unique styling issues.

This post tests overlay header images with custom `page.tagline`.

```yaml
tagline: "This is a custom tagline content which overrides the default page excerpt."
header:
  overlay_image: /assets/images/unsplash-image-1.jpg
  caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
```