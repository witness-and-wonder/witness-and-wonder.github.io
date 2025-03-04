---
layout: default
title: Witness & Wonder
layout_class: home
---

<ul class="post-list">
  {% assign sorted_testimonies = site.testimonies | sort: "date" | reverse %}
  {% for testimony in sorted_testimonies %}
    <li class="post-card">
      {% if testimony.thumbnail %}
      <div class="post-thumbnail">
        <img src="{{ testimony.thumbnail }}" alt="{{ testimony.title }} thumbnail">
      </div>
      {% endif %}
      <div class="post-content">
        <h2 class="post-title">
          <a href="{{ testimony.url }}">{{ testimony.title }}</a>
        </h2>
        <div class="post-meta">
          <small>{{ testimony.date | date: "%B %d, %Y" }}</small>
          {% if testimony.author %}
          <span class="post-author"> by {{ testimony.author }}</span>
          {% endif %}
        </div>
        {% if testimony.excerpt %}
        <p>{{ testimony.excerpt }}</p>
        {% endif %}
        {% if testimony.tags %}
        <div class="post-tags">
          {% for tag in testimony.tags %}
          <span>{{ tag }}</span>
          {% endfor %}
        </div>
        {% endif %}
      </div>
    </li>
  {% endfor %}
</ul>
