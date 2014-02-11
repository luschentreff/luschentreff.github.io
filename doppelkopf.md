---
layout: page
title: Doppelkopf
tagline: Doppelkopfer hierher
group: navigation
---
{% include JB/setup %}

<div class="col-md-12">
  <div class="category-header">
    <h2>Der Doppelkopf-Bereich</h2>
    <ul class="tag_box inline">
      {% assign pages_list = site.categories['doppelkopf'] %}
      {% include JB/pages_list %}
    </ul>
  </div>

  <p>Alle Beiträge zum Thema Doppelkopf:</p>
</div>

<div class="posts col-md-12">
  {% for post in site.categories['doppelkopf'] %}
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
</div>
