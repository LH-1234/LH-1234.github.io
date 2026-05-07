---
layout: default
title: 文章归档
permalink: /archive/   #指定地址，/archive/,如果不写，就是/archive.html
---

# 文章归档

{% if site.posts.size > 0 %}
{% for post in site.posts %}
- {{ post.date | date: "%Y-%m-%d" }} — [{{ post.title }}]({{ post.url | relative_url }})
{% endfor %}
{% else %}
暂无文章。
{% endif %}