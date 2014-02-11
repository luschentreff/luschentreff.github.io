---
layout: page
title: Blog
tagline: In diesem Blog erfahrt ihr alles was man über Kartenspielen wissen muss, kann und sollte.
group: navigation
---
{% include JB/setup %}

{{ site.tagline }}

<div class="posts col-md-12">
  {% for post in site.posts limit:5 %}
  <div class="article row">
    <div class="page-header col-md-12">
      <h1>{{ post.title }}</h1>
    </div>
    <div class="main col-md-8">
      {{ post.content }}
      <p><a href="{{ BASE_PATH }}{{ post.url }}">…weiter lesen</a></p>
    </div>
    <div class="col-md-4">
      <div class="col-md-12 meta-tag">
        <span class="date">{{ post.date | date_to_string }}</span><br />
        <span>von Cliff</span>
        <div class="social-media">
          <a href="#" class="fa fa-google-plus">&nbsp;</a>
          <a href="#" class="fa fa-facebook-square">&nbsp;</a>
          <a href="#" class="fa fa-twitter">&nbsp;</a>
        </div>
      </div>
    </div>
  </div>
  {% endfor %}

  <p><a href="{{ BASE_PATH }}/archive.html">Alle Blogbeiträge lesen</a></p>
</div>

