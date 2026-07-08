---
layout: page
title: projects
permalink: /projects/
description: A growing collection of your cool projects.
nav: false
display_categories: [work, fun]
horizontal: false
---

<!-- pages/projects.md -->
<div class="projects">
{% if site.enable_project_categories and site.display_categories %}
  <!-- Display categorized projects -->
  {% for category in site.display_categories %}
  <h2 class="category">{{ category }}</h2>
  {% assign categorized_projects = site.projects | where: "category", category %}
  {% assign sorted_projects = categorized_projects | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if site.enable_masonry %}
  <div class="grid">
    {% for project in sorted_projects %}
      {% include projects.html %}
    {% endfor %}
  </div>
  {% else %}
  <div class="row">
    {% for project in sorted_projects %}
      <div class="col-sm-6">
        {% include projects.html %}
      </div>
    {% endfor %}
  </div>
  {% endif %}
  {% endfor %}

{% else %}

<!-- Display projects without categories -->
{% assign sorted_projects = site.projects | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if site.enable_masonry %}
  <div class="grid">
    {% for project in sorted_projects %}
      {% include projects.html %}
    {% endfor %}
  </div>
  {% else %}
  <div class="row">
    {% for project in sorted_projects %}
      <div class="col-sm-6">
        {% include projects.html %}
      </div>
    {% endfor %}
  </div>
  {% endif %}
{% endif %}
</div>
