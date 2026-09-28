---
layout: page
title: Projects
permalink: /projects/
description: Selected research and engineering projects across devices, hardware, and embodied AI.
nav: true
nav_order: 4
display_categories: [research, systems]
horizontal: false
---

<div class="projects">
{% for category in page.display_categories %}
  <h2 class="category">{{ category | capitalize }}</h2>
  {% assign categorized_projects = site.projects | where: "category", category %}
  {% assign sorted_projects = categorized_projects | sort: "importance" %}
  <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
{% endfor %}
</div>
