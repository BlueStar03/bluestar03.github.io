---
layout: home
---

[Destiny Saga](/destiny-saga/)


Below is a list of all collections available on this site:

{% for collection in site.collections %}
  {% if collection[0] != 'posts' %}  <!-- Exclude the default 'posts' collection -->
    ## {{ collection[0] | capitalize }}

    [Browse the {{ collection[0] | capitalize }} collection]({{ site.baseurl }}/{{ collection[0] }}/)

    {% for item in collection[1] %}
      - [{{ item.title }}]({{ item.url }})
    {% endfor %}

  {% endif %}
{% endfor %}
