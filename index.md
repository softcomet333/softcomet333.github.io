---
title: softcomet333
permalink: /
layout: default
---

<h2 class="directory-heading">~/</h2>

<div class="directory">

  <a class="file-row folder-row" href="#archive">
    <span class="file-icon">📁</span>
    <span>_archive</span>
    <span class="file-kind">文件夹</span>
  </a>

  <div id="archive" class="directory-children">
    {% assign entries = site.archive | sort: "date" | reverse %}
    {% for entry in entries %}
    <a class="file-row" href="{{ entry.url | relative_url }}">
      <span class="file-icon">📄</span>
      <span class="file-name">{{ entry.name | escape | remove: ".md" }}</span>
      <span class="file-kind">Markdown</span>
    </a>
    {% endfor %}
  </div>

</div>