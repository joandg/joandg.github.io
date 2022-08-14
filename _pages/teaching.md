---
layout: page
title: Teaching
permalink: /Teaching/
description: Teaching activities
nav: true
nav_order: 4
---
<div class="teaching">
<h3 class="category">B.Sc. in Mathematics</h3>
<hr>
</div>
* 2019-2020: Professor responsible of classroom [Large scale data management](http://miei.di.uminho.pt/plano_estudos.html#cd_gestao_de_grandes_conjuntos_de_dados), Universidade do Minho
* 2015-2016: Professor of Distributed Computing in the [MAP-i](https://mapi.map.edu.pt/) Doctoral Programme in University of Aveiro
* 2010-2011: Professor responsible of classroom Operating Systems and Distributed systems in CET de Redes at Instituto Politécnico do Cávado e do Ave (IPCA).
* 2009-2010: Professor of classroom practice of EISD, Distributed Systems, Universidade do Minho
* 2008-2009: Professor of classroom practice of EISD, Distributed Systems, Universidade do Minho 


<div class="teaching">
<h2 class="category">ongoing courses</h2>
<div class="grid">
  {% assign sorted_teaching = site.teaching | sort: "runningindex" | reverse %}
  {% for teaching in sorted_teaching %}
    {% if teaching.category == "course" and teaching.status == "ongoing" %}
      {% include courses.html %}
    {% endif %}
  {% endfor %}
</div>

<h2 class="category">planned courses</h2>
<div class="grid">
  {% assign sorted_teaching = site.teaching | sort: "runningindex" | reverse %}
  {% for teaching in sorted_teaching %}
    {% if teaching.category == "course" and teaching.status == "planned" %}
      {% include courses.html %}
    {% endif %}
  {% endfor %}
</div>

<h2 class="category">archive courses</h2>
<div class="grid">
  {% assign sorted_teaching = site.teaching | sort: "runningindex" | reverse %}
  {% for teaching in sorted_teaching %}
    {% if teaching.category == "course" and teaching.status == "archive" %}
      {% include courses.html %}
    {% endif %}
  {% endfor %}
</div>

</div>


---
layout: page_course
university: tud
semester: Q1 & Q2 2022/2023
title: Linear Algebra and Optimisation for Machine Learning
instructors: Alexander Heinlein and Krzysztof Postek
description:
runningindex: 18
nolink: true
category: course
status: planned
---
