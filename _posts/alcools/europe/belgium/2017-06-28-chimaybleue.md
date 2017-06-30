---
layout: page
sidebar: right
subheadline: Bière trapiste
title:  "Chimay bleue"
teaser: "This is the best rhum EVER."
breadcrumb: true
tags:
    - belgium
    - bière
    - trapiste
categories:
    - alcools
country: Belgique
image:
    thumb: gallery-example-2-thumb.jpg
    title: gallery-example-2.jpg
    caption: Unsplash.com
    caption_url: http://unsplash.com
---
*Feeling Responsive* shows metadata by default. The default behaviour can be changed via `config.yml`. To show metadata at the end of a page/post just add the following to front matter:
<!--more-->

~~~
show_meta: true
~~~

If you don't want to show metadata, it's simple again:

~~~
show_meta: false
~~~

## Autres alcools de {{ page.country }}
{: .t60 }
{% include list-posts tag='alcools' %}
