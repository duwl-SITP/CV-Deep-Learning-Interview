---
layout: default
title: index
permalink: /record/index.html
---

## Record Archive

{% assign entries = site.pages | where_exp: "item", "item.dir == '/record/'" | sort: "title" | reverse %}
{% for entry in entries %}
- [{{ entry.title }}]({{ entry.url | relative_url }})
{% endfor %}
