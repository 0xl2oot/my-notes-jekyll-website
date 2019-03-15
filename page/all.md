---
layout: page
title: 全部文章
permalink: /all/
---

{% for post in site.posts %}
  <h4><a href="{{ post.url }}">{{ post.title }}</a></h4>
{% endfor %}