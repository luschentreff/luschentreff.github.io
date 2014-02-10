---
layout: page
title: Kartenspielen
tagline: Hier sind alle Kartenspiele vereint
group: navigation
weight: 1
---
{% include JB/setup %}

<div class="category-header">
  <h2>Hier sind alle Kartenspiele vereint</h2>
  <ul class="tag_box inline">
    {% assign pages_list = site.categories['kartenspielen'] %}
    {% include JB/pages_list %}
  </ul>
</div>

Alle Beiträge zum Thema Kartenspiele:

<div class="posts">
  {% for post in site.categories['kartenspielen'] %}
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
