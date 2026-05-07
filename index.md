---
layout: default   #文章的homepage
title: homepage
---

# 锁链的homepage

这里是我的个人文章与记录网站

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

## 更多

- [查看全部文章]({{ "/archive/" | relative_url }})
指向归档路径
- [关于我]({{ "/about/" | relative_url }})