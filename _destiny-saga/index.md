---
title: "Index of Files"
---

# Destiny Saga

Below is a list of all chapters in the saga, organized by category:

{% assign grouped_files = site.destiny-saga %}

{% assign categories = "" %}

{% for file in grouped_files %}
  {% assign folder = file.path | split: '/' | first %}

  {% unless categories contains folder %}
    {% assign categories = categories | append: folder | append: "," %}
    <h2>{{ folder | capitalize }}</h2>
    <ul>
  {% endunless %}

  {% if file.path contains folder %}
    <li>
      <a href="{{ file.url }}">{{ file.title }}</a>
    </li>
  {% endif %}
  
  {% if forloop.last %}
    </ul>
  {% endif %}
{% endfor %}

---

date: 2025-01-11 19:21:00 -0800
author: "zBuLe"
description: "Description of the Corlee people"

