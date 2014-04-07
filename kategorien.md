---
layout: page
title: Categories
header: Alle Beiträge nach Kategorien sortiert
sitemap:
  priority: 0.7
  changefreq: weekly
  lastmod: 2014-04-07T10:56:19+02:00
---
{% include JB/setup %}

<ul class="tag_box inline">
  {% assign categories_list = site.categories %}
  {% include JB/categories_list %}
</ul>


{% for category in site.categories %} 
  <h2 id="{{ category[0] }}-ref">{{ category[0] | join: "/" }}</h2>
  <ul>
    {% assign pages_list = category[1] %}  
    {% include JB/pages_list %}
  </ul>
{% endfor %}

