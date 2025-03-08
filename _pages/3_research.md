---
layout: page
permalink: /research/
title: Research
description: 
nav: true
nav_order: 
display_categories: [work, fun]
horizontal: false
---


We are exploring several exciting research directions, often with overlapping boundaries.


<!-- pages/projects.md -->
<div class="projects">
{% if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {% for category in page.display_categories %}
  <a id="{{ category }}" href=".#{{ category }}">
    <h2 class="category">{{ category }}</h2>
  </a>
  {% assign categorized_projects = site.projects | where: "category", category %}
  {% assign sorted_projects = categorized_projects | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal %}
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.html %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_projects %}
      {% include projects.html %}
    {% endfor %}
  </div>
  {% endif %}
  {% endfor %}

{% else %}

<!-- Display projects without categories -->

{% assign sorted_projects = site.projects | sort: "importance" %}

  <!-- Generate cards for each project -->

{% if page.horizontal %}

  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.html %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_projects %}
      {% include projects.html %}
    {% endfor %}
  </div>
  {% endif %}
{% endif %}
</div>

<br>

---


### **Experimental facility** 

The Laboratory for Engineered Materials and Structures (LEMS) is dedicated to the design of phononic crystals and metamaterials, as well as the precise measurement of their vibration and wave properties. The laboratory is equipped with advanced tools, including a laser Doppler vibrometer (LDV), a vibration shaker, a 3D printer, a mini-universal testing machine (mini-UTM), high-frequency piezo-actuators and sensors with associated electronic equipment.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/research/LEMS.png" title="example image" class="img-fluid  z-depth-0" %}
    </div>
</div>

<br>

---

### **Our sponsors**

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/research/Sponsors.png" title="Group Photo, April 2023" class="img-fluid  z-depth-0" %}
    </div>
</div>
