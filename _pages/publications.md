---
layout: page
permalink: /Publications/
title: Publications
# description:
years: [2022,2021,2019,2018,2017,2016,2015,2014,2013]
nav: true
nav_order: 2
---
An up-to-date list is available in my [Google Scholar](https://scholar.google.com/citations?user=IgKAJBwAAAAJ).

<!-- _pages/publications.md -->
<div class="publications">

{%- for y in page.years %}
  <h4 class="year">{{y}}</h4>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
