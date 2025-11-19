---
layout: page
title: Research
permalink: /research/
nav: true
nav_order: 3
# display_categories: [work, fun]
horizontal: false
---

The new space era is defined by rapidly decreasing launch costs from heavy-lift rockets such as Starship and New Glenn, and an ever-growing demand for spacecraft with increased capabilities. Nonetheless, modern spacecraft are limited by the constraints of launch: they must fit within the volume of the rocket fairing, survive accelerations up to 50 g, and deploy with perfect precision in orbit. Achieving ambitious future missions – such as large space telescopes for exoplanet detection and the construction of planetary infrastructure – requires breakthroughs in how we design, build, and launch structures to space.

In-space assembly and manufacturing (ISAM) offer a promising path forward by enabling the robotic construction of structures directly in space. ISAM can produce systems that are larger and better optimized for loads in the space environment, transforming science missions, enabling next-generation space stations, and paving the way for permanent infrastructure on the Moon and Mars. ISAM is on the verge of space demonstrations with recent advances in robotic construction, but critical challenges remain before it is routinely integrated into missions:

 - Candidate ISAM processes have **high size, weight, and power requirements**, limiting their integration with small spacecraft.
 - **Precise structures** are difficult to construct with open-loop ISAM processes.
 - The changes in mass properties over long timescales of construction pose challenges to **spacecraft attitude control**.

The SPARC Lab tackles these challenges through interdisciplinary research in mechanics, dynamics, and robotics. We aim to develop the fundamental technologies for efficient and precise ISAM, demonstrate them through ground- and space-based experiments, and enable the construction of large-scale infrastructure on orbit and on planetary surfaces.

<!-- Display focus areas as cards -->
<h3 class="black-section-heading">Current Focus Areas</h3>
<div class="projects">
{% assign sorted_projects = site.projects | sort: "importance" %}
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
</div>

<!-- Collaborator logos -->
<h3 class="black-section-heading">Collaborators</h3>

<div class="collaborator-logos">
  <img src="{{ '/assets/img/logos/MITlogo_cut.png' | relative_url }}" alt="MIT">
  <img src="{{ '/assets/img/logos/NASAlogo.png' | relative_url }}" alt="NASA">
  <img src="{{ '/assets/img/logos/JPLlogo_cut.png' | relative_url }}" alt="JPL">
  <img src="{{ '/assets/img/logos/NGClogo.png' | relative_url }}" alt="Northrop Grumman">
  <img src="{{ '/assets/img/logos/APLlogo_cut.png' | relative_url }}" alt="APL">
  <img src="{{ '/assets/img/logos/MITLLlogo.png' | relative_url }}" alt="MIT Lincoln Laboratory">
</div>

<style>
.collaborator-logos {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  gap: 2rem;
  margin: 2rem 0;
  max-width: 100%;
}

.collaborator-logos img {
  height: 55px;
  width: auto;
  object-fit: contain;
  filter: grayscale(0%);
  opacity: 1;
}

/* Make specific logos smaller for visual balance */
.collaborator-logos img[alt="Northrop Grumman"],
.collaborator-logos img[alt="JPL"] {
  height: 45px;
}
/* Make specific logos smaller for visual balance */
.collaborator-logos img[alt="MIT Lincoln Laboratory"] {
  height: 50px;
}


@media (max-width: 768px) {
  .collaborator-logos img {
    height: 50px;
  }
}
</style>