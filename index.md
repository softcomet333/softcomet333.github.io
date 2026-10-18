---
layout: default
title: softcomet333
permalink: /
---

<div class="intro">

# 你好.

这是一个小小的个人站

随便存一些东西.

</div>

<div class="section-label">
  NOTES / ARCHIVE INDEX
</div>

<div class="archive-list">
{% assign entries = site.archive | sort: "date" | reverse %}
{% for entry in entries %}
  <a class="archive-item" href="{{ entry.url | relative_url }}">
    <span class="archive-title">
      {{ entry.title | default: entry.name | escape }}
    </span>
    {% if entry.date %}
      <span class="archive-meta">
        {{ entry.date | date: "%Y-%m-%d" }}
      </span>
    {% endif %}
    {% if entry.description %}
      <span class="archive-description">
        {{ entry.description | escape }}
      </span>
    {% endif %}
  </a>
{% endfor %}
</div>

<p class="archive-meta">
  TOTAL RECORDS: {{ entries.size }}
</p>
