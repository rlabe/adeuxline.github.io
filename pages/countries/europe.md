---
layout: page
show_meta: false
title: "Europe"
subheadline: "Il y en a beaucoup..."
header:
   image_fullwidth: "header_unsplash_5.jpg"
permalink: "/countries/europe/"
---
<ul>
    {% for post in site.categories.countries %}
    {% if post.subheadline == "europe" %}
    <li><a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
    {% endif %}
    {% endfor %}
</ul>
