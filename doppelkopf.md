---
layout: page
title: Doppelkopf
tagline: Doppelkopfer hierher
group: navigation
---
{% include JB/setup %}

<div class="category-header">
  <h2>Der Doppelkopf-Bereich</h2>
  <ul class="tag_box inline">
    {% assign pages_list = site.categories['Doppelkopf'] %}
    {% include JB/pages_list %}
  </ul>
</div>

Alle Beiträge zum Thema Doppelkopf:

<div class="posts">
  {% for post in site.categories['Doppelkopf'] %}
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
