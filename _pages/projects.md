---
layout: page
title: Research
permalink: /projects/
description: >
  The new space era is defined by rapidly decreasing launch costs from heavy-lift rockets such as Starship and New Glenn, and an ever-growing demand for spacecraft with increased capabilities. Nonetheless, modern spacecraft are limited by the constraints of launch: they must fit within the volume of the rocket fairing, survive accelerations up to 50 g, and deploy with perfect precision in orbit. Achieving ambitious future missions – such as large space telescopes for exoplanet detection and the construction of planetary infrastructure – requires breakthroughs in how we design, build, and launch structures to space.

  In-space assembly and manufacturing (ISAM) offer a promising path forward by enabling the robotic construction of structures directly in space. ISAM can produce systems that are larger and better optimized for loads in the space environment, transforming science missions, enabling next-generation space stations, and paving the way for permanent infrastructure on the Moon and Mars. ISAM is on the verge of space demonstrations with recent advances in robotic construction, but critical challenges remain before it is routinely integrated into missions:

  •	Candidate ISAM processes have high size, weight, and power requirements, limiting their integration with small spacecraft.
  •	Precise structures are difficult to construct with open-loop ISAM processes.
  •	The changes in mass properties over long timescales of construction pose challenges to spacecraft attitude control.

  The SPARC Lab tackles these challenges through interdisciplinary research in mechanics, dynamics, and robotics. We aim to develop the fundamental technologies for efficient and precise ISAM, demonstrate them through ground and space-based experiments, and enable the construction of large-scale infrastructure in orbit and on planetary surfaces.
nav: true
nav_order: 3
display_categories: [work, fun]
horizontal: false
---

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
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
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
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
{% endif %}
</div>
