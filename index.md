---
layout: default  
title: welcome
---

## 欢迎来到校长的个人博客

{% assign featured_posts = site.posts | where: "featured_home", true %}

{% if featured_posts.size > 0 %}
<section class="home-section">
  <h2>精选文章</h2>

  <div class="post-grid">
    {% for post in featured_posts limit:3 %}
      <article class="post-card">
        <time>{{ post.date | date: "%Y-%m-%d" }}</time>
        <h3>
          <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        </h3>
        <p>{{ post.excerpt | strip_html | truncate: 80 }}</p>
      </article>
    {% endfor %}
  </div>
</section>
{% endif %}

## 最新文章

<div class="post-grid latest-post-grid">
{% for post in site.posts limit:3 %}
  <a class="post-card latest-post-card" href="{{ post.url | relative_url }}">
    <article>
      <div class="post-card-top">
        <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%Y-%m-%d" }}</time>
        <span>0{{ forloop.index }}</span>
      </div>
      <h3>{{ post.title }}</h3>
    </article>
  </a>
{% endfor %}
</div>

## 更多

- [回到首页]({{ "/" | relative_url }})
- [全部文章]({{ "/archive/" | relative_url }})
- [关于本站]({{ "/about/" | relative_url }})
