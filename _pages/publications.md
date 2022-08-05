---
layout: page
permalink: /publications/
title: publications
description: publications by categories in reversed chronological order. 
years: [2013...2020]
nav: true
nav_order: 1
---
<!-- _pages/publications.md -->
<div class="publications">

{%- for y in 2013:2024 %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
