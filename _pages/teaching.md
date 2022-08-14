---
layout: page
title: Teaching
permalink: /Teaching/
description: Teaching materials.
nav: true
nav_order: 4
display_categories: ["B.Sc. in Mathematics", "B.Sc. in Chemistry", "B.Sc. in Computer Science"]
horizontal: false
---
<div class="projects">
  {% if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
    {% for category in page.display_categories %}
      <h2 class="category">{{ category }}</h2>
      {% assign categorized_teaching = site.teaching | where: "category", category %}
      {% assign sorted_teaching = categorized_teaching | sort: "importance" %}
      <!-- Generate cards for each project -->
      {% if page.horizontal %}
        <div class="container">
          <div class="row row-cols-2">
          {% for teaching in sorted_teaching %}
            {% include teaching_horizontal.html %}
          {% endfor %}
          </div>
        </div>
      {% else %}
        <div class="grid">
          {% for project in sorted_teaching %}
            {% include teaching.html %}
          {% endfor %}
        </div>
      {% endif %}
    {% endfor %}

  {% else %}
  <!-- Display teaching without categories -->
    {% assign sorted_teaching = site.teaching | sort: "importance" %}
    <!-- Generate cards for each teaching -->
    {% if page.horizontal %}
      <div class="container">
        <div class="row row-cols-2">
        {% for project in sorted_teaching %}
          {% include teaching_horizontal.html %}
        {% endfor %}
        </div>
      </div>
    {% else %}
      <div class="grid">
        {% for project in sorted_teaching %}
          {% include teaching.html %}
        {% endfor %}
      </div>
    {% endif %}

  {% endif %}

</div>
