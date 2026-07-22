---
layout: page
permalink: /publications/
title: Publications
description: publications by categories in reversed chronological order.
nav: true
nav_order: 2
---

<!-- _pages/publications.md -->

<!-- Bibsearch Feature -->

{% include bib_search.liquid %}

## Articles

<div class="publications">
{% bibliography --query @*[keywords *= article] %}
</div>

## Talks

<div class="publications">
{% bibliography --query @*[keywords *= talk] %}
</div>
