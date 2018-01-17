---
layout: page
show_meta: false
title: "Ils parlent de nous !"
header:
   image_fullwidth: "header_homepage_13.jpg"
permalink: "/journaux/"
---

<center><div class="container">
  <table class="table table-striped">
    <thead>
      <tr>
        <th>Date</th>
        <th>Journal</th>
        <th>Titre</th>
	<th>Lien</th>
      </tr>
    </thead>
    <tbody>
      
	{% for article in site.data.presse %}
	<tr>	
		<td> {{article.date}}</td>
		<td> {{article.journal}}</td>
		<td> {{article.titre}} </td>
		<td><a href="{{article.lien}}">Lire l'article</a></td>
	</tr>
	{% endfor %}
      
    </tbody>
  </table>
</div></center>
