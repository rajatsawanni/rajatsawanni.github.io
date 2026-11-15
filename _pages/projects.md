---
layout: page
title: Research
permalink: /projects/
description: Facilities, diagnostics and models for gas-to-particle processes in extreme environments
nav: true
nav_order: 2
display_categories: ["Facilities and experiments", "Modeling and analysis tools", "Ongoing projects", "Earlier work"]
horizontal: false
---

<!-- pages/projects.md -->

My research asks one question: **how do transport phenomena, chemical kinetics and multi-phase microphysics couple during gas-to-particle transformations in extreme environments?** I have studied it in two experimental regimes, high-pressure soot formation and low-pressure, low-temperature contrail formation, by building the facilities, optical diagnostics and numerical tools needed to measure these processes under controlled conditions. The projects below describe this work.

## Research directions

My future research will follow combustion particles through their life cycle, from their formation in flames to their activation in clouds, in three thrusts:

- **Soot and emissions of future fuels:** sooting tendencies and soot morphology, maturity and chemistry of sustainable aviation fuels, hydrogen, ammonia and oxygenated blends at elevated pressures, with validation targets for combustion models.
- **Cloud condensation and contrail formation:** ice-nucleation rates on combustion particles along mixing lines, the effect of fuel composition on contrail-forming aerosols, and ice nucleation on a chip with in-situ electron microscopy.
- **Spray flames and nanoparticle synthesis:** using soot chemistry and nucleation microphysics to make carbon nanomaterials by pyrolysis and spray-flame synthesis.
<div class="projects">
{% if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {% for category in page.display_categories %}
  <a id="{{ category | slugify }}" href=".#{{ category | slugify }}">
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
