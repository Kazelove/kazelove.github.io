---
layout: page
title: Welcome to "Not Wached"
tagline: a blog that you didnt see because you didnt look
---
{% include JB/setup %}

## current post:

{% for post in site.posts limit:1 %}
<span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a>
<p>{{post.content}}</p>
{% endfor %}

## posts list:

<ul class="posts">
  {% for post in site.posts offset:1 limit:5 %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>
