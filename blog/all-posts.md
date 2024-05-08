# Blog Posts Archive

{% for post in site.posts %}
  {%- assign post_date = post.date | date: "%Y-%m-%d %I:%M %P" -%}
  <h3>{{ post_date }}: <a href="{{ post.url }}">{{ post.title }}</a></h3>
{% endfor %}

----

## [Blog Home](./index.md)
