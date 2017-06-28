---
layout: page
show_meta: false
title: "Liste des pays !"
subheadline: "Il y en a beaucoup..."
header:
   image_fullwidth: "header_unsplash_5.jpg"
permalink: "/countries/"
---
<ul>
    {% for post in site.categories.countries.europe %}
    <li><a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
</ul>
