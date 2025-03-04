---
layout: home
title: Witness & Wonder
---

<section class="testimonies">
  {% for testimony in site.testiomnies %}
    <article class="testimony">
      <h2><a href="{{ testimony.url }}">{{ testimony.title }}</a></h2>
      <small>{{ testimony.date | date_to_string }}</small>
      <p>{{ testimony.excerpt }}</p>
    </article>
  {% endfor %}
</section>
