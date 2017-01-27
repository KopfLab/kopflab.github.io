---
layout: default
menu: Home
icon: fa fa-home
title: Geobiology & Geomicrobial Physiology at CU Boulder
title_height: 100px
image:
  - file: /header_images/home/santa_paula_creek_oil_seep_lowres.jpg
    title: Microbial communities<br/>near natural oil seeps
    location: Santa Paula Creek, California
  - file: /header_images/home/yellowstone_lowres.jpg
    title: Carbonate terraces<br/>at Mammoth hot springs
    location: Yellowstone National Park, Wyoming
  - file: /header_images/home/rmnp_methane_bubbles_lowres.jpg
    title: Methane bubbles frozen in ice
    location: Rocky Mountain National Park, Colorado
  - file: /header_images/home/mono_lake.jpg
    title: Alkaline Mono Lake
    location: Eastern Sierra Nevada, California
  - file: /header_images/home/stromatolites.jpg
    title: Precambrian Chevron<br/>Stromatolites
    location: West Texas
  - file: /header_images/home/iceland.jpg
    title: Phototrophs growing<br/>in glacial melt
    location: Laugavegur, Iceland
  - file: /header_images/home/octopus_spring.jpg
    title: Microbial structures at<br/>Octopus Spring
    location: Yellowstone National Park, Wyoming
image_height: 300px
image_interval: 3000
weight: 0
category: home
---

## About the Lab

The Geomicrobial Physiology lab at the University of Colorado Boulder started in the Fall of 2016 and is focused on studying the physiological drivers of geochemical fingerprints of microbial metabolism, particularly isotopic effects and molecular markers. The lab is part of the newly expanding Geobiology program in the <a href="http://www.colorado.edu/geolsci/">Department of Geological Sciences</a> at CU Boulder, that also comprises <a href="http://spot.colorado.edu/~templeta/Templeton_Lab/Welcome.html" target="new">Alexis Templeton's</a>, <a href="https://instaar.colorado.edu/people/julio-sepulveda/" target="new">Julio Sepulveda's</a>, Boswell Wing's and <a href="http://isotope.colorado.edu/" target="new">Steve Mojzsis'</a> groups, and has close ties with the Institute of Arctic and Alpine Research (<a href="https://instaar.colorado.edu/" target="new">INSTAAR</a>) and the <a href="https://biofrontiers.colorado.edu/" target="new">Biofrontiers Institute</a>. Please note that this website is still under construction and more information will follow soon. In the meantime, please contact sebastian.kopf (at) colorado.edu about upcoming research opportunities at CU Boulder.

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
