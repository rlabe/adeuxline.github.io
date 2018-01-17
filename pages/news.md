---
layout: page_full
show_meta: false
title: "Toutes les nouvelles !"
header:
   image_fullwidth: "header_homepage_13.jpg"
permalink: "/news/"
---

<center><div class="container">
  <table class="table table-striped">
    <thead>
      <tr>
        <th>Date</th>
        <th>Titre</th>
        <th>Teaser</th>
	<th>Article</th>
      </tr>
    </thead>
    <tbody>
      
	{% for new in site.data.news %}
	<tr>	
		<td> {{new.date}}</td>
		<td> {{new.title}}</td>
		<td> {{new.teaser}} </td>
		<td>{% if new.lien %} <a href="{{new.lien}}">Lire l'article</a>{% endif %}</td>
	</tr>
	{% endfor %}
      
    </tbody>
  </table>
</div></center>
