---
layout: page
title: Skat
tagline: Skatspieler hierher
group: navigation
---
{% include JB/setup %}

<h2>Der Schafkopf-Bereich</h2>

<ul class="tag_box inline">
  {% assign pages_list = site.categories['skat'] %}
  {% include JB/pages_list %}
</ul>

Alle Beiträge zum Thema Skat:

<ul class="posts">
  {% for post in site.categories['skat'] %}
    <h2>{{ post.title }}</h2>
    {{ post.content }}
    <p><a href="{{ BASE_PATH }}{{ post.url }}">...weiter lesen</a></p>
    <p>Cliff, {{ post.date | date_to_string }}</p>
  {% endfor %}
</ul>