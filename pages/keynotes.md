---

title: Speakers
layout: event_noheader
permalink: /program/keynotes/

---
# {{page.title}}
<br>
<div class="keynote-full">
<!-- {% assign sorted_speakers = site.data.keynotespeakers | sort: "name" %} -->
{% assign shuffled_speakers = site.data.keynotespeakers | shuffle %}

{% for speaker in sorted_speakers %}
<hr>
		{% if speaker.name %}
		<div>
		    <a name="{{speaker.name}}"><img style="background-image: url(/assets/images/speakers/{{speaker.image | default: 'owasp_logo.png'}});{{speaker.style}};"></a>
		</div>
		<div class='keynote-info'>
			<a><strong>{{speaker.name}}</strong></a>
			<br>
			{{speaker.bio}}
			<br>
			{% if speaker.title %}
				<strong>Charla:</strong> {{ speaker.title }}
				<br>
			{% endif %}
			{% if speaker.subject %}
				<strong>Taller:</strong> {{ speaker.subject}}
			{% endif %}
			<br>
			{% if speaker.abstract %}
				<strong>Abstract:</strong>{{ speaker.abstract }}
			{% endif %}
		</div>
		{% endif %}
{% endfor %}
</div>
