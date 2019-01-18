---
layout: post
title:  "Jekyll 中代码块显示 Liquid 代码"
description: "Jekyll 中代码块显示 Liquid 代码"
category: "Jekyll"
tags: ["Jekyll", "Liquid"]
date:   2018-10-27 21:30:00 +0800
---

在写关于 Jekyll 模板的文章的时候发现 Liquid 代码无法在文章中正确显示


这个时候可以这样写

![](/assets/Screen Shot 2018-10-27 at 9.44.18 PM.png)

这样就能显示出来啦~~~


```html
{% raw %}

<!-- This loops through the paginated posts -->
{% for post in paginator.posts %}
  <h1><a href="{{ post.url }}">{{ post.title }}</a></h1>
  <p class="author">
    <span class="date">{{ post.date | date_to_rfc822 }}</span>
  </p>
  <div class="content">
    {{ post.content | strip_html |truncate:210,'...' }}
  </div>
  <br>
{% endfor %}

{% endraw %}
```
