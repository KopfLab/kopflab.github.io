---
layout: default
menu: Home
icon: fa fa-home
title: Geobiology & Geomicrobial Physiology at CU Boulder
title_height: 100px
image:
  - file: /images/header/home/santa_paula_creek_oil_seep_lowres.jpg
    title: Microbial communities<br/>near natural oil seeps
    location: Santa Paula Creek, California
  - file: /images/header/home/yellowstone_lowres.jpg
    title: Carbonate terraces<br/>at Mammoth hot springs
    location: Yellowstone National Park, Wyoming
  - file: /images/header/home/rmnp_methane_bubbles_lowres.jpg
    title: Methane bubbles frozen in ice
    location: Rocky Mountain National Park, Colorado
  - file: /images/header/home/mono_lake.jpg
    title: Alkaline Mono Lake
    location: Eastern Sierra Nevada, California
  - file: /images/header/home/stromatolites.jpg
    title: Precambrian Chevron<br/>Stromatolites
    location: West Texas
  - file: /images/header/home/iceland.jpg
    title: Phototrophs growing<br/>in glacial melt
    location: Laugavegur, Iceland
  - file: /images/header/home/octopus_spring.jpg
    title: Microbial structures at<br/>Octopus Spring
    location: Yellowstone National Park, Wyoming
image_height: 300px
image_interval: 3000
weight: 0
category: home
---

## About the Lab

The Geomicrobial Physiology lab at CU Boulder consists of a [diverse group of researchers](/people) from the geological, environmental and microbiological sciences focused on discovering how microorganisms grow in their natural habitats, how they respond to environmental change, and how they produce various types of molecular and isotopic biomarkers - traces of life that are preserved in the environment for millions and sometimes billions of years. The combination of these three lines of scientific inquiry enables us to better reconstruct past environments and helps us predict how microbial life will respond to future change. We also do a fair bit of tools development for geochemical data processing and experimental design in microbiology and strive to make all of our lab designs and software open-source and easily available to advance the pace of discovery. Check out our [research](/research), [publications](/publications) and [resources](/resources) for more information.


## Recent News

{% for post in site.categories.news limit: site.front_page_news %}
<div class="news-item media">
  <div class="media-left">
    <div class="news-date">
      <div class="day">{{ post.date | date: "%-d"}}</div>
      <div class="month">{{ post.date | date: "%B"}}</div>
      <div class="year">{{ post.date | date: "%Y"}}</div>
    </div>
  </div>

  <div class="media-body">
    <h3 class="media-heading"><a href="{{ post.url }}">{{ post.title }}</a></h3>
    {{ post.content | strip_html | truncatewords: 50 }}
    {% assign post_length = post.content | number_of_words %}
    {% if post_length > 50 %}
    <a href="{{ post.url }}"><strong>read more</strong></a>
    {% endif %}
  </div>
</div>
{% endfor %}
