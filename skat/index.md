---
layout: page
title: Skat
tagline: Skatspieler hierher
group: navigation
---
{% include JB/setup %}

<div class="col-md-12">
  <div class="category-header">
    <h2>Der Skat-Bereich</h2>
    <ul class="tag_box inline">
      {% assign pages_list = site.categories['skat'] %}
      {% include JB/pages_list %}
    </ul>
  </div>

  <p>Alle Beiträge zum Thema Skat:</p>
</div>

<div class="posts col-md-12">
  <p>Hier findest Du alle Beiträge, die sich dem Thema Skat widmen</p>
  {% for post in site.categories['skat'] %}
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
          <span>Cliff</span>
          <div class="social-media">
            <a href="https://plus.google.com/share?url=http://www.luschentreff.de" class="fa fa-google-plus" target="_blank">&nbsp;</a>
            <a href="http://www.facebook.com/sharer.php?u=www.luschentreff.de" class="fa fa-facebook-square" target="_blank">&nbsp;</a>
            <a href="http://twitter.com/share?url=http://www.luschentreff" class="fa fa-twitter" target="_blank">&nbsp;</a>
          </div>
        </div>
      </div>
    </div>
  {% endfor %}
</div>
