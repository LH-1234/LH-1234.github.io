---
layout: default
title: 文章归档
permalink: /archive/
---

# 文章归档

## [entertainment]({{ "/featured/entertainment/" | relative_url }})

{% assign entertainment_posts = site.posts | where: "featured", "entertainment" %}

{% if entertainment_posts.size > 0 %}
共 {{ entertainment_posts.size }} 篇文章。

{% for post in entertainment_posts %}
- {{ post.date | date: "%Y-%m-%d" }} — [{{ post.title }}]({{ post.url | relative_url }})
{% endfor %}
{% else %}
暂无文章。
{% endif %}

## [game-anime]({{ "/featured/game-anime/" | relative_url }})

{% assign game_anime_posts = site.posts | where: "featured", "game-anime" %}

{% if game_anime_posts.size > 0 %}
共 {{ game_anime_posts.size }} 篇文章。

{% for post in game_anime_posts %}
- {{ post.date | date: "%Y-%m-%d" }} — [{{ post.title }}]({{ post.url | relative_url }})
{% endfor %}
{% else %}
暂无文章。
{% endif %}

## [learn]({{ "/featured/learn/" | relative_url }})

{% assign learn_posts = site.posts | where: "featured", "learn" %}

{% if learn_posts.size > 0 %}
共 {{ learn_posts.size }} 篇文章。

{% for post in learn_posts %}
- {{ post.date | date: "%Y-%m-%d" }} — [{{ post.title }}]({{ post.url | relative_url }})
{% endfor %}
{% else %}
暂无文章。
{% endif %}
