---
layout: page
permalink: /publications/
title: Publications
description: Journal articles, conference papers and talks, newest first.
nav: true
nav_order: 3
---

<!-- _pages/publications.md -->

<!-- Bibsearch Feature -->

{% include bib_search.liquid %}

## Journal Articles

<div class="publications">
{% bibliography -f papers -q @article %}
</div>

## Conference Papers

<div class="publications">
{% bibliography -f papers -q @inproceedings %}
</div>

## Conference Presentations

<div class="publications">
{% bibliography -f talks %}
</div>
