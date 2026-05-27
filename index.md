---
layout: default
title: Record Index
permalink: /
---

## Record

按日期浏览：

{% for entry in site.pages reversed %}
{% if entry.dir == '/record/' and entry.path != 'record/index.md' %}
- [{{ entry.title }}]({{ entry.url | relative_url }})
{% endif %}
{% endfor %}

## README

- [Repository README](./README.html)
