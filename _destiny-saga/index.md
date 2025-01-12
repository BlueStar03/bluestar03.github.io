---
title: "Index of Files"
---

# Destiny Saga Index

Here are all the chapters in the Destiny Saga, grouped by category:

{% assign folders = "chronicle-destiny,threa,people" | split: "," %}

{% for folder in folders %}
  {% assign folder_items = site.destiny-saga | where_exp: "item", "item.path contains '/#{folder}/'" %}
  
  {% if folder_items.size > 0 %}
    ## {{ folder | capitalize }}

    <ul>
      {% for item in folder_items %}
        <li><a href="{{ item.url }}">{{ item.title }}</a></li>
      {% endfor %}
    </ul>
  {% endif %}
{% endfor %}

---

---

---

date: 2025-01-11 19:21:00 -0800  

