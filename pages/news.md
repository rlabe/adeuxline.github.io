---
layout: page
show_meta: false
title: "Toutes les nouvelles !"
header:
   image_fullwidth: "header_homepage_13.jpg"
permalink: "/news/"
---

<ul class="side-nav">

		{% for new in site.data.news %}
			<strong>{{ new.date }}</strong> - {{ new.title }} - {% if new.teaser %}{{ new.teaser }}{% endif %}{% if new.lien %} - <a href="{{ site.url }}{{ site.baseurl }}/#/">Plus d'infos</a>{% endif %}<br/>
		{% endfor %}

</ul>
