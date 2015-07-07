---
layout: page
title: Blog
permalink: /blog/
---

<div class="post-list">
  {% for post in site.posts %}
  <section class="section">
  <h2>
    <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
  </h2>
  <h5><span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span></h5>
  <p>
  {% if post.excerpt %}{{ post.excerpt | strip_html | strip_newlines | truncate: 300 }}{% else %}{{ site.description }}{% endif %}
  </p>
  </section>
  {% endfor %}
</div>
