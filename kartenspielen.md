---
layout: page
title: Kartenspielen
tagline: Hier sind alle Kartenspiele vereint
group: navigation
weight: 1
---
{% include JB/setup %}

<h2>Hier sind alle Kartenspiele vereint</h2>

<ul class="tag_box inline">
  {% assign pages_list = site.categories['kartenspielen'] %}
  {% include JB/pages_list %}
</ul>

Alle Beiträge zum Thema Schafkopf:

<ul class="posts">
  {% for post in site.categories['kartenspielen'] %}
    <h2>{{ post.title }}</h2>
    {{ post.content }}
    <p><a href="{{ BASE_PATH }}{{ post.url }}">...weiter lesen</a></p>
    <p>Cliff, {{ post.date | date_to_string }}</p>
  {% endfor %}
</ul>