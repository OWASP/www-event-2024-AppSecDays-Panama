---
title: Appsec Day Panama Team
layout: event_noheader
permalink: /team/
---

# {{ page.title }}

<link rel="stylesheet" href="/assets/css/team.css">

<br>
<div class="team-container">
  {% for member in site.data.team %}
  <div class="team-card">
    <div class="team-image" style="background-image: url('/assets/images/team/{{member.image}}');"></div>
    <div class="team-info">
      <h3>{{ member.name }}</h3>
      <p>{{ member.role }}</p>
    </div>
  </div>
  {% endfor %}
</div>
