---
layout: page
title: Posts
tagline:
---

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
      {% if post.description %}
        <span class="body">{{ post.description | strip_html }}</span>
      {% else %}
        <span class="body">{{ post.excerpt | strip_html }}</span>
      {% endif %}
    <br/>
  {% endfor %}
</ul>