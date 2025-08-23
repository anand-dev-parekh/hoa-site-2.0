---
layout: page
title: News
permalink: /news/
---

<h2>News & Notices</h2>

{% if site.posts.size > 0 %}
  <ul class="news-list">
  {% for post in site.posts %}
    <li>
      <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
      <small class="muted">{{ post.date | date: "%B %e, %Y" }}</small>
      <p>{{ post.excerpt | strip_html | truncate: 240 }}</p>
    </li>
  {% endfor %}
  </ul>
{% else %}
  <p>No news yet.</p>
{% endif %}