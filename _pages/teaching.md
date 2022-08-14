---
layout: page
permalink: /teaching/
title: Teaching
description: A brief list of courses I have taught since 2013/2014 at UIB.
nav: true
nav_order: 4
---

All materials can be downloaded from UIB Digital. You are required to be a student at the Universitat de les Illes Balears (UIB) and be enrolled in the corresponding course to have access to all data.


<div class="publications">

{% assign grouped_courses = site.teaching | group_by: "last_year" | sort: "name" | reverse %}
{% for course_year in grouped_courses %}
  
  {% assign year_courses_sorted = course_year.items | sort: "importance" %}
  {% for course in year_courses_sorted %}

    <h2 class="year">
    {% if course.first_year != course.last_year %} {{ course.first_year }}-{% endif %}{{ course.last_year }} ({{ course.times }}x)</h2>
    <div class="row">
      <div class="col-sm-2 abbr">
        <a href="{{ course.course_url }}" title="{{ course.course_full }}" class="badge {{course.course_color}}">{{ course.course }}</a>
      </div>
      <div class="col-sm-8">
        <div><b>{{ course.title }} ({{ course.level }})</b></div>
        <div>
          <em>{{course.role}}</em>
        </div>
        <div>
          <b>Topics:</b> {{ course.topics }}
        </div>
      </div>
    </div>
  {% endfor %}
    
{% endfor %}

</div>
