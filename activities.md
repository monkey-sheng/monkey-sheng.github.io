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
## {{ post_year }}
{% assign previous_year = post_year %}
{% assign previous_month = "" %}
{% endif %}
{% if month_key != previous_month %}
### {{ post_month }}
{% assign previous_month = month_key %}
{% endif %}
- [{{ post.title }}]({{ site.github.url }}{{ post.url }}) — {{ post.date | date: "%B %-d, %Y" }}
{% endfor %}
