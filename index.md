---
layout: page
title: Blog
tagline: In diesem Blog erfahrt ihr alles was man über Kartenspielen wissen muss, kann und sollte.
group: navigation
---
{% include JB/setup %}



{{ site.tagline }}

<div class="posts">
  {% for post in site.posts limit:5 %}
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

<p><a href="{{ BASE_PATH }}/archive.html">Alle Blogbeiträge lesen</a></p>

