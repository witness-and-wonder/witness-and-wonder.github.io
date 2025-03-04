---
layout: default
title: Witness & Wonder
---

<h1>{{ page.title }}</h1>

<ul>
  {% assign sorted_testimonies = site.testimonies | sort: "date" | reverse %}
  {% for testimony in sorted_testimonies %}
    <li>
      <a href="{{ testimony.url }}">{{ testimony.title }}</a>
      <small>{{ testimony.date | date: "%B %d, %Y" }}</small>
    </li>
  {% endfor %}
</ul>
