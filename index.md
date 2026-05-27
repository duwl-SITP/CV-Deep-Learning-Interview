---
layout: default
title: Record Index
permalink: /
---

## Record

Browse by date:

<div class="record-list">
{% for entry in site.pages reversed %}
{% if entry.dir == '/record/' %}
{% if entry.url != '/record/index.html' %}
{% assign sections = entry.content | markdownify | split: '<h2' %}
<a class="record-card" href="{{ entry.url | relative_url }}">
  <p class="record-card__title">{{ entry.title }}</p>
  <p class="record-card__meta">Questions: {{ entry.questions }}{% if entry.source %} | Source: {{ entry.source }}{% endif %}</p>
  <div class="record-card__summary">
    <ul class="record-card__topics">
      {% for section in sections offset:1 %}
      {% assign heading = section | split: '</h2>' | first | split: '>' | last | strip_html | strip %}
      {% if heading != '' %}
      <li>{{ heading }}</li>
      {% endif %}
      {% endfor %}
    </ul>
  </div>
</a>
{% endif %}
{% endif %}
{% endfor %}
</div>

## README

- [Repository README](./README.html)
