---
title: "Index of Files"
---

# Destiny Saga

Below is a list of all items in the Destiny Saga collection, grouped by their respective categories:

{% assign grouped_items = site.destiny-saga | group_by: "dir" %}

{% for group in grouped_items %}
  <h2>{{ group.name | capitalize }}</h2>
  <ul>
    {% for item in group.items %}
      <li><a href="{{ item.url }}">{{ item.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}

date: 2025-01-11 19:21:00 -0800  

