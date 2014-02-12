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
      <p><a href="{{ BASE_PATH }}{{ post.url }}">Beitrag lesen</a></p>
    </div>
    <div class="col-md-4">
      <div class="col-md-12 meta-tag">
        <span class="date">
          <!-- Whitespace added for readability -->
          {% assign m = page.date | date: "%-m" %}
          {{ page.date | date: "%-d." }}
          {% case m %}
            {% when '1' %}Januar
            {% when '2' %}Februar
            {% when '3' %}M&auml;rz
            {% when '4' %}April
            {% when '5' %}Mai
            {% when '6' %}Juni
            {% when '7' %}Juli
            {% when '8' %}August
            {% when '9' %}September
            {% when '10' %}Oktober
            {% when '11' %}November
            {% when '12' %}Dezember
          {% endcase %}
          {{ page.date | date: "%Y" }}
        </span><br />
        <span>Cliff</span>
        <div class="social-media">
          <a href="#" class="fa fa-google-plus">&nbsp;</a>
          <a href="#" class="fa fa-facebook-square">&nbsp;</a>
          <a href="#" class="fa fa-twitter">&nbsp;</a>
        </div>
      </div>
    </div>
  </div>
  {% endfor %}

  <p><a href="{{ BASE_PATH }}/archiv">Alle Blogbeiträge lesen</a></p>
</div>

