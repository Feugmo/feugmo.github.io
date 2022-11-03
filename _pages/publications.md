---
layout: page
permalink: /publications/
title: publications
description: List of our publications
years: [2012, 2013, 2015, 2017, 2019, 2021, 2022]
nav: true
nav_order: 2
---
<!-- _pages/publications.md -->
<div class="publications">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
