---
layout: categories
permalink: /books/
title: Books
search_exclude: true
---
{% for post in site.categories['book'] %}
  {% if post.hide != true %}
  {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
  <article class="archive-item">
    <p class="post-meta post-meta-title"><a class="page-meta" href="{{ site.baseurl }}{{ post.url }}">{{post.title}}</a>  • {{ post.date | date: date_format }}</p>
  </article>
  {% endif %}
{% endfor %}
