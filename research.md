---
layout: post-index
title: Research
---

<!-- Below you'll find explanations on how to create a site just like this and get it hosted
  for free.  -->
{% for post in site.posts %}
  {% if post.tags contains "research" %}
- **[{{ post.title }}]({{ post.url }})**

  {{ post.excerpt }}

  {% endif %}
{% endfor %}

<!-- # COMMENT EXPLAINING THIS PAGE -- 
We're currently using this section of the site to host these tutorials,
  but you might want to use it to showcase and describe your `Research`,
  to chronicle various `Talks` you've given over your history, or to
  write about various news or updates that have happened to you.

You can update the `title` of file (line 3) to change the heading of 
  the page and its title in the browser. To change how it's referred to
  in the navigation and/or adjust its url, see `data/navigation.yml` file.
-->


