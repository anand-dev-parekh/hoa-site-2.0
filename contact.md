---
layout: page
title: Contact
permalink: /contact/
---

<!-- Page hero injected -->
<div class="page-hero">
  <img src="{{ '/assets/images/contact-hero.jpg' | relative_url }}" alt="Get in Touch">
  <div class="page-hero__overlay"><h1>Get in Touch</h1></div>
</div>


## Contact Us

Have a question or need to report an issue? Send us a message.

<!-- Use Formspree (free tier) or your own handler and replace YOUR_FORM_ID below -->
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
  <p>
    <label>Name<br>
      <input type="text" name="name" required>
    </label>
  </p>
  <p>
    <label>Email<br>
      <input type="email" name="email" required>
    </label>
  </p>
  <p>
    <label>Message<br>
      <textarea name="message" rows="6" required></textarea>
    </label>
  </p>
  <p><button type="submit">Send</button></p>
</form>

<p class="muted">Or email us at <a href="mailto:contact@example.com">contact@example.com</a>.</p>

<!-- Contact map -->
<figure class="figure">
  <img src="{{ '/assets/images/map-placeholder.jpg' | relative_url }}" alt="Map of Maple Grove neighborhood">
  <figcaption>Find us near the main park entrance.</figcaption>
</figure>
