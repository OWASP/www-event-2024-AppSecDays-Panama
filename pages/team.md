---
title: "Appsec Day Panama Team"
layout: event_noheader
permalink: /team/
---

<link rel="stylesheet" href="/assets/css/team.css">

# {{page.title}}

<div class="team-container">
  {% for member in site.data.team %}
    <div class="team-card">
      <img src="/assets/images/team/{{ member.image }}" alt="{{ member.name }}">
      <div class="team-info">
        <h3>{{ member.name }}</h3>
        <p>{{ member.role }}</p>
      </div>
    </div>
  {% endfor %}
</div>
