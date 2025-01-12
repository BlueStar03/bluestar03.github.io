---
title: "Index of Files"
---

# Destiny Saga

Below is a list of all chapters in the saga, organized by category:

{% assign grouped_by_folder = site.destiny-saga | group_by: "dir" %}

{% for folder in grouped_by_folder %}
  <h2>{{ folder.name | capitalize }}</h2>
  <ul>
    {% for item in folder.items %}
      <li>
        <a href="{{ item.url }}">{{ item.title }}</a>
      </li>
    {% endfor %}
  </ul>
{% endfor %}

date: 2025-01-11 19:21:00 -0800
author: "zBuLe"
description: "Description of the Corlee people"

