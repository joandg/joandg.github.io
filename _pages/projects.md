---
layout: page
title: Projects
permalink: /Projects/
# description: A growing collection of your cool projects.
nav: true
nav_order: 3
display_categories: [work, fun]
horizontal: false
---
Coming soon...

<!-- 
<div class="projects">
{%- if site.enable_project_categories and page.display_categories %}
  
  {%- for category in page.display_categories %}
  <h5 class="category">{{ category }}</h5>
  {%- assign categorized_projects = site.projects | where: "category", category -%}
  {%- assign sorted_projects = categorized_projects | sort: "importance" %}
  
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_projects -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
  {% endfor %}

{%- else -%}

  {%- assign sorted_projects = site.projects | sort: "importance" -%}

  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_projects -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
{%- endif -%}
</div>
-->
