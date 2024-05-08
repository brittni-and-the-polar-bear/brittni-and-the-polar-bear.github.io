# Archive Tags

{% assign tag_names = "" %}
{% for tag in site.tags %}
  {% assign tag_names = tag_names | append: tag[0] %}
  {% assign tag_names = tag_names | append: "|" %}
{% endfor %}

{% assign all_tags = tag_names | split: "|" %}
{% assign sorted_tags = all_tags | sort_natural %}

{% for tag in sorted_tags %}
  {%- assign tag_filename = tag | downcase | replace: " ", "-" -%}
  <h3><a href="./posts-by-tag/{{ tag_filename }}.html">{{ tag }}</a></h3>
{% endfor %}

----

## [Blog Home](./index.md)
