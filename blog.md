---
layout: default
title: Blog
permalink: /blog/
---
<style>
.posts{
    padding: 0;
}
</style>

<h1>Writings & Thoughts <a class="twitter-follow-button"
  href="https://twitter.com/zeyadetman"
  data-size="small"></a></h1>
<ul class="posts">
  {% for post in site.posts %}
    <li>
        <a href=" {{post.url}} ">{{post.title}}</a>
        <p>{{post.date | date: "%b %d, %Y"}} • <span>{{post.categories}}</span></p>
    </li>
  {% endfor %}
</ul>