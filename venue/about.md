---
title: "Venue"
layout: event_noheader
permalink: /venue/about/
---

<link rel="stylesheet" href="/assets/css/venue.css">

# {{ site.data.venue.title }}

<div class="venue-section">
  <h2>{{ site.data.venue.location_name }}</h2>
  <p><strong>Dirección:</strong> {{ site.data.venue.address }}</p>
  
  <div class="venue-content">
    <div class="venue-map">
      <iframe src="{{ site.data.venue.map_url }}" width="100%" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
    </div>
    <div class="venue-description">
      <img src="/assets/images/venue/{{ site.data.venue.image }}" alt="Venue Image">
      <p>{{ site.data.venue.description }}</p>
    </div>
  </div>

  <div class="venue-details">
    {% for section in site.data.venue.sections %}
      <div class="venue-section-card">
        <h3>{{ section.title }}</h3>
        <img src="/assets/images/venue/{{ section.image }}" alt="{{ section.title }} Image">
        <p>{{ section.description }}</p>
      </div>
    {% endfor %}
  </div>
</div>
