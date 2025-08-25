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

<!-- Officers grid -->
<section class="officers-grid">
  <h2>Board & Officers</h2>
  <div class="officers-grid__wrap">
    {%- for o in site.data.officers -%}
      {%- assign slug = o.image | default: o.name | downcase | replace: ' ', '-' | replace: '.', '' | replace: ',', '' -%}
      <article class="officer-card">
        <img src="{{ '/assets/images/officers/' | relative_url }}{{ slug }}.jpg" alt="{{ o.name }} headshot">
        <div class="officer-card__body">
          <h3>{{ o.name }}</h3>
          {%- if o.role -%}<p class="muted">{{ o.role }}</p>{%- endif -%}
          {%- if o.email -%}<p><a href="mailto:{{ o.email }}">{{ o.email }}</a></p>{%- endif -%}
        </div>
      </article>
    {%- endfor -%}
  </div>
</section>
