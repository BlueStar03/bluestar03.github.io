---
title: "Destiny Saga"
date: 2025-01-11 21:15:00 -0800
author: "zBuLe"
description: "Everything about Destiny Saga"
---

# Destiny Saga Files

{% assign grouped_files = site.destiny-saga | group_by_exp: "file", "file.path | split: '/' | last | prepend: file.path | split: '/' | slice: 0, -1 | join: '/'" %}

<ul>
{% for group in grouped_files %}
  <li>
    <strong>{{ group.name }}</strong>
    <ul>
      {% for file in group.items %}
        <li><a href="{{ file.url }}">{{ file.title }}</a></li>
      {% endfor %}
    </ul>
  </li>
{% endfor %}
</ul>
