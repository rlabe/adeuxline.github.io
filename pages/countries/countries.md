---
layout: blog_countries
title: "Liste des pays"
teaser: "Il y a beaucoup de pays."
breadcrumb: false
header:
   image_fullwidth: header_unsplash_1.jpg
permalink: "countries/"
---
{% assign category = 'countries' %}

 {% if category %}

    {% for post in site.categories.[category] %}
<div class="row">
    <div class="small-12 columns b60">
      <h2><a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h2>
      <p>
        {% if post.image.thumb %}<a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}" title="{{ post.title | escape_once }}"><img src="{{ site.urlimg }}{{ post.image.thumb }}" class="alignleft" width="150" height="150" alt="{{ page.title escape_once }}"></a>{% endif %}

        {% if post.meta_description %}{{ post.meta_description | strip_html | escape }}{% elsif post.teaser %}{{ post.teaser | strip_html | escape }}{% endif %}

        <a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}" title="{{ site.data.language.read }} {{ post.title | escape_once }}"><strong>{{ site.data.language.read_more }}</strong></a>
      </p>
    </div><!-- /.small-12.columns -->
  </div><!-- /.row -->
    {% endfor %}

  {% endif %}
