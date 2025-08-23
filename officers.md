---
layout: page
title: Officers
permalink: /officers/
---

<h2>Board Officers</h2>
<ul class="cards">
{% for person in site.data.officers.officers %}
  <li class="card">
    <h3>{{ person.name }}</h3>
    <p class="muted">{{ person.role }}</p>
    {% if person.email %}<p><a href="mailto:{{ person.email }}">{{ person.email }}</a></p>{% endif %}
    {% if person.phone %}<p>{{ person.phone }}</p>{% endif %}
  </li>
{% endfor %}
</ul>