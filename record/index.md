---
layout: default
title: index
permalink: /record/index.html
---

## Record Archive

{% assign pages_sorted = site.pages | sort: "name" | reverse %}

{% for entry in pages_sorted %}
  {% if entry.path contains 'record/' and entry.path != 'record/index.md' %}
- [{{ entry.title | default: entry.name }}]({{ entry.url | relative_url }})
  {% endif %}
{% endfor %}
