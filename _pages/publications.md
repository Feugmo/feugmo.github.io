---
layout: page
permalink: /publications/
title: publications
description: List of our publications
years: [2022, 2021,  2019, 2017, 2015, 2013, 2012]
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
