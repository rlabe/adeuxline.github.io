---
layout: page
show_meta: false
title: "Europe"
subheadline: "Il y en a beaucoup..."
header:
   image_fullwidth: "header_unsplash_5.jpg"
permalink: "/countries/europe/"
---

{% assign category = 'countries' %}
{% assign tag = 'europe' %}
<ul class="side-nav">

  {% if category == NULL and tag == NULL %}

    {% for post in site.posts limit:include.entries offset:include.offset %}
      <li><a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}">{% if post.subheadline %}{{ post.subheadline }} &middot; {% endif %}<strong>{{ post.title }}</strong></a></li>
    {% endfor %}
      <li class="text-right"><a href="{{ site.url }}{{ site.baseurl }}/blog/archive/"><strong>{{ site.data.language.more }}</strong></a></li>


  {% elsif category %}

    {% for post in site.categories.[category] limit:include.entries offset:include.offset %}
      <li><a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}">{% if post.subheadline %}{{ post.subheadline }} &middot; {% endif %}<strong>{{ post.title }}</strong></a></li>
    {% endfor %}
      <li class="text-right"><a href="{{ site.url }}{{ site.baseurl }}/blog/archive/"><strong>{{ site.data.language.more }}</strong></a></li>


  {% elsif tag %}

    {% for post in site.tags.[tag] limit:include.entries %}
      <li><a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}">{% if post.subheadline %}{{ post.subheadline }} &middot; {% endif %}<strong>{{ post.title }}</strong></a></li>
    {% endfor %}

  {% endif %}
</ul>
