---

title: Schedule & Trainings
layout: event_noheader
permalink: /trainings/

---
# {{page.title}}

#### Training subject to change based on trainer availability and meeting the number of students per trainer request.

## Pricing
1-day course : $freebr>
2-day course: $free<br>


AppSec Days Panamá 2024
<br><br>
1-day training courses will be held on September 11.

<section class='training'>
{% if site.data.trainings.size > 0 %}
{% assign trainings = site.data.trainings | sort: 'Title' %}
{% for trainer in trainings %}
<section class="trainer-section" id="{{trainer.SectionId}}">
<hr>
<ul>
<li><h3 class='training-header'>{{ trainer.Title }}<button class="cta-button grey" {%if trainer.Status == 'Postponed' or trainer.Status == 'Canceled' or trainer.Status == 'Booked Out' %}disabled='true' {%endif%} onclick="location.href='{{trainer.URL}}';" style="margin-left:1em;cursor: pointer;max-width=80px;">{%if trainer.Status == 'Postponed' or trainer.Status == 'Canceled' or trainer.Status == 'Booked Out'%}{{trainer.Status}}{%else%}Join Us{%endif%}</button></h3></li>
<li class="training-desc">{{ trainer.Description }}</li>
    <ul>
        {% for tr in trainer.Trainers %}
        <li><div class="training-container"><a href="/trainers/#{{tr.TrainerId}}" title="{{tr.Biography | strip_html}}"><div class="training-image" style="background-image:url('{{tr.Image}}');"></div>{{tr.Name}}</a></div></li>
        {% endfor %}
    </ul>
</ul>
</section>
{% endfor %}
{% endif %}
</section>
