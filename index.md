---
layout: home
title: "City Data Strategies"
author_profile: false
---

## City Strategies

<div style="display: grid; grid-template-columns: repeat(auto-fill, minmax(300px, 1fr)); gap: 20px;">
  {% for city in site.cities %}
    <div style="border: 1px solid #ddd; padding: 16px; border-radius: 8px; box-shadow: 0 2px 8px rgba(0,0,0,0.1);">
      {% if city.thumbnail %}
        <a href="{{ city.url }}">
          <img src="{{ city.thumbnail }}" alt="{{ city.city }} thumbnail" style="width: 100%; height: 200px; object-fit: cover; border-radius: 4px;">
        </a>
      {% endif %}
      <h3>
        <a href="{{ city.url }}">{{ city.city }}, {{ city.country }}</a>
      </h3>
      {% if city.summary %}
        <p>{{ city.summary | truncatewords: 20 }}</p>
      {% endif %}
      <p><strong>Status:</strong> {{ city.status }}</p>
    </div>
  {% endfor %}
</div>

