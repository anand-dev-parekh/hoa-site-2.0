---
layout: default
title: Home
---

<section class="hero">
  <h2>Welcome to {{ site.title }}</h2>
  <p>{{ site.description }}</p>
</section>

<section class="news-preview">
  <h3>Latest News</h3>
  {% assign latest = site.posts | slice: 0, 3 %}
  {% if latest.size > 0 %}
    <ul class="news-list">
      {% for post in latest %}
        <li>
          <h4><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h4>
          <small class="muted">{{ post.date | date: "%B %e, %Y" }}</small>
          <p>{{ post.excerpt | strip_html | truncate: 180 }}</p>
        </li>
      {% endfor %}
    </ul>
    <p><a href="{{ '/news/' | relative_url }}">See all news →</a></p>
  {% else %}
    <p>No news yet. Add your first post in <code>_posts/</code>.</p>
  {% endif %}
</section>