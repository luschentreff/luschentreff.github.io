---
layout: page
title: Schnapsen
tagline: Schnapser hierher
group: navigation
---
{% include JB/setup %}

<div class="category-header">
  <h2>Der Schnapsen-Bereich</h2>
  <ul class="tag_box inline">
    {% assign pages_list = site.categories['schnapsen'] %}
    {% include JB/pages_list %}
  </ul>
</div>

Alle Beiträge zum Thema Schnapsen:

<div class="posts">
  {% for post in site.categories['schnapsen'] %}
    <div class="article">
      <div class="page-header">
        <h1>{{ post.title }}</h1>
        <p class="meta-tag">{{ post.date | date_to_string }}, von Cliff</p>
      </div>
      {{ post.content }}
      <p><a href="{{ BASE_PATH }}{{ post.url }}">…weiter lesen</a></p>
    </div>
  {% endfor %}
</div>
