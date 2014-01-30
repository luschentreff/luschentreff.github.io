---
layout: page
title: Schafkopf
tagline: Schafkopfer hierher
group: navigation
---
{% include JB/setup %}

<h2>Der Schafkopf-Bereich</h2>

<ul class="tag_box inline">
  {% assign pages_list = site.categories['schafkopf'] %}
  {% include JB/pages_list %}
</ul>

Alle Beiträge zum Thema Schafkopf:

<div class="posts">
  {% for post in site.categories['schafkopf'] %}
    <h2>{{ post.title }}</h2>
    {{ post.content }}
    <p><a href="{{ BASE_PATH }}{{ post.url }}">...weiter lesen</a></p>
    <p>Cliff, {{ post.date | date_to_string }}</p>
  {% endfor %}
</div>
