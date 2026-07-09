---
layout: page
title: "News"
permalink: /blog/
---

<ul class="post-list">
{% for post in site.posts %}
  <li>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    <time>{{ post.date | date: "%B %-d, %Y" }}</time>
  </li>
{% endfor %}
</ul>
