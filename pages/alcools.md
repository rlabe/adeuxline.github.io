---
layout: page
show_meta: false
title: "Alcool!"
subheadline: "GLOUGLOU"
header:
   image_fullwidth: "header_unsplash_5.jpg"
permalink: "/alcools/"
---
<ul>
    {% for post in site.categories.alcools %}
    <li><a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
</ul>
