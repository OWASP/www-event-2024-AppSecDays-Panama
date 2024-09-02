---

title: Appsec Day Panama Team
layout: event_noheader
permalink: /team/

---
# {{page.title}}
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>{{ page.title }}</title>
    <link rel="stylesheet" href="/assets/css/team.css">
    <style>
        /* Aquí también puedes poner CSS adicional específico para esta página */
    </style>
</head>

<br>
<div class="team-container">
  {% for member in site.data.team %}
  <div class="team-card">
    <div class="team-image" style="background-image: url('/assets/images/{{member.image}}');"></div>
    <div class="team-info">
      <h3>{{ member.name }}</h3>
      <p>{{ member.role }}</p>
    </div>
  </div>
  {% endfor %}
</div>