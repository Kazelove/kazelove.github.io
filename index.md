---
layout: page
title: Welcome to "Not Wached"
tagline: a blog that you didnt see because you didnt look
---
{% include JB/setup %}

## Current posts:

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a><p>{{post.content}}</p></li>
  {% endfor %}
</ul>
