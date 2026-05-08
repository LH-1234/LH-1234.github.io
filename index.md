---
layout: default  
title: welcome
---

## 欢迎来到校长的个人博客

## 精选文章

{% assign featured_posts = site.posts | where: "featured", true %}

{% if featured_posts.size > 0 %}

{% for post in featured_posts %}
- [{{ post.title }}]({{ post.url | relative_url }})  
  <small>{{ post.date | date: "%Y-%m-%d" }}</small>
{% endfor %}
{% else %}
暂无精选文章。
{% endif %}

## 最新文章

{% if site.posts.size > 0 %}
{% for post in site.posts limit:3 %}
- {{ post.date | date: "%Y-%m-%d" }} — [{{ post.title }}]({{ post.url | relative_url }})
{% endfor %}
{% else %}
暂无文章。
{% endif %}

## 更多

- [回到首页]({{ "/index/" | relative_url }})
- [全部文章]({{ "/archive/" | relative_url }})
- [关于本站]({{ "/about/" | relative_url }})