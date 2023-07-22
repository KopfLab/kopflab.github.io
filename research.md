---
layout: default
icon: fa fa-area-chart
weight: 2
title: Research
title_height: 80px
image:
  - file: /images/header/research/sfa_ned.jpg
    title: Colorimetric assay for<br/>nitrite quantification
  - file: /images/header/research/chemostat.jpg
    title: Chemostats<br/>in operation
  - file: /images/header/research/phototrophs.jpg
    title: Anoxygenic phototroph<br/>enrichment cultures
  - file: /images/header/research/cooler.jpg
    title: Peltier cooler assembly<br/>for temperature experiments
image_height: 200px
category: research
permalink: /research/
---

## Active Research Projects

{% assign projects = site.research | sort:"weight" %}
{% for project in projects %}
  {% include list_item.html item=project %}
{% endfor %}
