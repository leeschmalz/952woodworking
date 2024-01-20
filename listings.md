---
layout: default
title: Furniture Listings
---

<div class="furniture-listings">
  {% for item in site.data.listings %}
    <div class="furniture-item">
      <h2>{{ item.name }}</h2>
      <img src="{{ item.image }}" alt="{{ item.name }}">
      <p>{{ item.description }}</p>
      <p><strong>Price: ${{ item.price }}</strong></p>
    </div>
  {% endfor %}
</div>