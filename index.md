---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---
# Destiny Saga

Below is a list of all chapters in the saga:

{% for chapter in site.destiny-saga %}
- [{{ chapter.title }}]({{ chapter.url }})
{% endfor %}