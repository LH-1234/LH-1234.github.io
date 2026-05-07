---
layout: default
title: 文章归档
permalink: /archive/
---

# 文章归档

{% if site.posts.size > 0 %}

{% for item in site.data.featured %}
## [{{ item.name }}]({{ item.url | relative_url }})

{% assign posts_in_featured = site.posts | where: "featured", item.key %}

{% if posts_in_featured.size > 0 %}
共 {{ posts_in_featured.size }} 篇文章。

{% for post in posts_in_featured %}
- {{ post.date | date: "%Y-%m-%d" }} — [{{ post.title }}]({{ post.url | relative_url }})
{% endfor %}
{% else %}
暂无文章。
{% endif %}

{% endfor %}

{% else %}

暂无文章。

{% endif %}