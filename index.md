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
    <h2>{{ post.title }}</h2>
    {{ post.content }}
    <p><a href="{{ BASE_PATH }}{{ post.url }}">...weiter lesen</a></p>
    <p>Cliff, {{ post.date | date_to_string }}</p>
  {% endfor %}
</div>

<p><a href="{{ BASE_PATH }}/archive.html">Alle Blogbeiträge lesen</a></p>

