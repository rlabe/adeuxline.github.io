---
layout: page
show_meta: false
title: "europe"
subheadline: "Il y en a beaucoup..."
header:
   image_fullwidth: "header_unsplash_5.jpg"
permalink: "/countries/europe/"
---
<ul>
    {% for post in site.categories.countries %}
    {% if post. %}
    <li><a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
</ul>
