---
layout: default
title: index
permalink: /record/index.html
---

## Record Archive

{% for entry in site.pages reversed %}
{% if entry.dir == '/record/' %}
{% if entry.url != '/record/index.html' %}
- [{{ entry.title | default: entry.name }}]({{ entry.url | relative_url }})
{% endif %}
{% endif %}
{% endfor %}
