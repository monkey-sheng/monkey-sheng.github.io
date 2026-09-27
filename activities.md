---
layout: page
title: Blogs
---

{% assign previous_year = "" %}
{% assign previous_month = "" %}
{% for post in site.categories.blog %}
  {% assign post_year = post.date | date: "%Y" %}
  {% assign post_month = post.date | date: "%B" %}
  {% assign month_key = post.date | date: "%Y-%m" %}
  {% if post_year != previous_year %}
    {% unless forloop.first %}</ul>{% endunless %}
    <h2>{{ post_year }}</h2>
    {% assign previous_year = post_year %}
    {% assign previous_month = "" %}
  {% endif %}
  {% if month_key != previous_month %}
    {% if previous_month != "" %}</ul>{% endif %}
    <h3>{{ post_month }}</h3>
    <ul class="blog-archive">
    {% assign previous_month = month_key %}
  {% endif %}
  <li>
    <a href="{{ site.github.url }}{{ post.url }}">{{ post.title }}</a>
    <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %-d, %Y" }}</time>
    {% if post.excerpt %}<p>{{ post.excerpt | strip_html | truncate: 180 }}</p>{% endif %}
  </li>
  {% if forloop.last %}</ul>{% endif %}
{% endfor %}
