{%- assign tag_name = "Twitter" -%}
{%- assign tag_match = tag_name | downcase -%}

<h1>Posts by Tag: {{ tag_name }}</h1>

{% for tag in site.tags %}
  {%- assign site_tag_name = tag[0] | downcase -%}
  {%- if site_tag_name == tag_match -%}
    {%- for post in tag[1] -%}
      {%- assign post_date = post.date | date: "%Y-%m-%d %I:%M %P" -%}
      <h3>{{ post_date }}: <a href="{{ post.url }}">{{ post.title }}</a></h3>
    {%- endfor -%}
  {%- endif -%}
{% endfor %}

----

## [Archive Tags](../all-tags.md)
