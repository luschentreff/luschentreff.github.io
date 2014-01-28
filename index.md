---
layout: page
title: Blog
tagline: Eine Seite von Luschen für Luschen - in diesem Blog erfahrt ihr alles was man über Kartenspielen wissen kann.
group: navigation
---
{% include JB/setup %}

{% for tag in site.tags %}
<li style="list-style: none; font-size: {{ tag | last | size | times: 100 | divided_by: tag[0].size | plus: 50 }}%">
  <a href="{{ BASE_PATH }}{{ site.JB.tags_path }}#{{ tag[0] }}-ref">{{ tag[0] }}</a>
</li>
{% endfor %}

<ul class="posts">
  {% for post in site.posts limit:5 %}
    <h2>{{ post.title }}</h2>
    {{ post.content }}
    <p><a href="{{ BASE_PATH }}{{ post.url }}">...weiter lesen</a></p>
    <p>Cliff, {{ post.date | date_to_string }}</p>
  {% endfor %}
</ul>

<p><a href="{{ BASE_PATH }}/archive.html">Alle Blogbeiträge lesen</a></p>

