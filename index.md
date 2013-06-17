---
layout: page
title: never give up
tagline: I do 
---
{% include JB/setup %}

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>
<div style="text-align:right;">
<img style="width:200px;" src="../img/me.png"/>
</div>
