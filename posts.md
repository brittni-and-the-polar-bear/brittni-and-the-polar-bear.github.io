---
title: posts
---

{% for post in site.posts %}
  {%- assign post_date = post.date | date: "%Y-%m-%d %I:%M %P" -%}
  <h3 style="margin-bottom: 0px;"><a href=".{{ post.url }}">{{ post.title }}</a></h3>
  <p><small>{{ post_date }}</small></p>
{% endfor %}
