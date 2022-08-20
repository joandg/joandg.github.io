---
layout: page
permalink: /Talks/
title: Talks
# description:
years: [2018,2017,2015,2014,2013,2012]
nav: true
nav_order: 5
# selected_talks: false # includes a list of talks marked as "selected={true}"
---
<div class="publications">
<p> This is a list of invited talks in conferences, workshops and seminars.</p>

{% if page.selected_papers %}
  {% include selected_papers.html %}
{% endif %}

{% for y in page.years %}
  <h5 class="year">{{y}}</h5>
  {% bibliography -f talks --query @misc[year={{y}}]* %}
{% endfor %}

</div>




