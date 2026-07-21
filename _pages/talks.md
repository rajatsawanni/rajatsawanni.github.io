---
layout: archive
title: "Talks"
permalink: /talks/
---

{% for talk in site.talks %}
  <h3>{{ talk.name }}</h3>
  <p><strong>Date:</strong> {{ talk.date }}</p>
  <p><strong>Location:</strong> {{ talk.location }}</p>
  <p>{{ talk.summary }}</p>
  <hr>
{% endfor %}
