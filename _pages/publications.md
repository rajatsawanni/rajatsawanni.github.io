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

## Manuscripts in Preparation

- **R. Sawanni**\*, A. Roy\*, Y. Rajan, C. C. Mayigue, T. Taddesse, I. Jahncke, S. Chaudhuri, C. P. T. Groth, Ö. L. Gülder. A contrail-in-a-lab facility to study the inception and development of contrails. _Bulletin of the American Meteorological Society_.
- A. Nobakht, **R. Sawanni**, Ö. L. Gülder. Effects of pressure on the chemical sooting structure of hydrogen doped ethylene counterflow diffusion flame. _Combustion and Flame_.
- A. E. Karataş, **R. Sawanni**, Ö. L. Gülder. Soot formation in high pressure diffusion flames. _Progress in Energy and Combustion Science_.

\* equal contributions

## Conference Presentations

<div class="publications">
{% bibliography -f talks %}
</div>
