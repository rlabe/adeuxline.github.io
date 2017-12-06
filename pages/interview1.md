---
layout: interview
show_meta: false
title: "interview1"
header:
   image_fullwidth: "header_unsplash_5.jpg"
permalink: "/interviews/"
---
{% assign job = site.data.interviews[page.title] %}

Interview de {{ job.intervenant }}.

L'interview se passe en {{ job.endroit }} en écoutant {{ job.musique }}.

<div class="panel">
	<ul>
	{% for qr in job.interview %}
		<li>{{ qr.question }}</li>
		<li>{{ qr.reponse }}</li>
	{% endfor %}
	</ul>
</div>
