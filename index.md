---
layout: default   #文章的homepage
title: homepage
---

# 一级标题，锁链的homepage

这里是我的个人文章与记录。

## 二级标题，精选文章

{% assign featured_posts = site.posts | where: "featured", true %}
% assign featured_posts = site.posts | where: "featured", true %，从所有文章site.posts中筛选出featured为true的文章，保存到featured_posts中


{% if featured_posts.size > 0 %}
% if featured_posts.size > 0 % ，如果featured_posts的大小大于0，说明有精选文章，执行后续命令

{% for post in featured_posts %}
- [{{ post.title }}]({{ post.url | relative_url }})  
  <small>{{ post.date | date: "%Y-%m-%d" }}</small>
{% endfor %}
{% else %}
暂无精选文章。
{% endif %}

% for post in featured_posts %,循环所有featured_posts值，按照标题：（相对路径）链接的方式展示，并且展示文章日期，small是表示小子号

## 更多

- [查看全部文章]({{ "/archive/" | relative_url }})
指向归档路径
- [关于我]({{ "/about/" | relative_url }})