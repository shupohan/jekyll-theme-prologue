---
layout: page
title: Reading List
icon: fa-book-open
order: 3
---

{% for category in site.categories %}
{%- if category[0] != 'my_blog' -%}
  <h3>{{ category[0] }}</h3>
  <ul>
    {% for post in category[1] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
  {%- endif -%}
{% endfor %}
