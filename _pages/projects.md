---
layout: page
title: Projects
permalink: /Projects/
# description: A growing collection of your cool projects.
nav: true
nav_order: 3
# display_categories: [work, fun]
horizontal: false
---

<div style="text-align: justify">
This is a list of research projects.
</div>

<div class="publications">
{% if page.selected_papers %}
  {% include selected_papers.html %}
{% endif %}

{% for y in page.years %}
  <h5 class="year">{{y}}</h5>
  {% bibliography -f talks -q @*[year={{y}}]* %}
{% endfor %}

</div>
