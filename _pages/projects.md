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

Most of what I work on comes back to one question: what happens when gases turn into particles under extreme conditions, inside a high-pressure flame or in the cold, thin air behind a cruising aircraft? Answering it usually means building the experiment first, then the diagnostics to look inside it, and then the models to explain what we see. Here are the main projects.

Looking ahead, I'd like to follow these particles through their whole life, from forming in a flame to seeding ice in a cloud. That means soot from new fuels like sustainable aviation fuels, hydrogen and ammonia; how those particles nucleate ice and form contrails (ideally watching it happen on a chip under an electron microscope); and using the same chemistry to make useful carbon nanomaterials.

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
