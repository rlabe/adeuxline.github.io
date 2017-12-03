---
layout: page
show_meta: false
title: "Statistiques"
header:
   image_fullwidth: "header_roadmap_3.jpg"
permalink: "/stats/"
---

<!-- Calculs -->
{% assign sum_superficie = 0 %}
{% for pays in site.data.countries %}
    {% assign sum_superficie = sum_superficie | plus: pays[1].superficie %}
{% endfor %}

{% assign total_jours = 0 %}
{% for pays in site.data.countries %}
    {% assign total_jours = total_jours | plus: pays[1].jourspasses %}
{% endfor %}

{% assign total_conducteurs = 0 %}
{% for pays in site.data.countries %}
    {% assign total_conducteurs = total_conducteurs | plus: pays[1].conducteurs %}
{% endfor %}

{% assign totale_distance = 0 %}
{% for pays in site.data.countries %}
    {% assign totale_distance = totale_distance | plus: pays[1].distance %}
{% endfor %}

{% assign km_voiture = 0 %}
{% for pays in site.data.countries %}
    {% assign km_voiture = km_voiture | plus: pays[1].km_voiture %}
{% endfor %}

{% assign km_camion = 0 %}
{% for pays in site.data.countries %}
    {% assign km_camion = km_camion | plus: pays[1].km_camion %}
{% endfor %}

{% assign km_bateau = 0 %}
{% for pays in site.data.countries %}
    {% assign km_bateau = km_bateau | plus: pays[1].km_bateau %}
{% endfor %}

{% assign total_cartes = 0 %}
{% for pays in site.data.countries %}
    {% assign total_cartes = total_cartes | plus: pays[1].cartes_postales %}
{% endfor %}

{% assign total_nuits_dehors = 0 %}
{% for pays in site.data.countries %}
    {% assign total_nuits_dehors = total_nuits_dehors | plus: pays[1].nuits_dehors %}
{% endfor %}

{% assign compteur_attente = 0 %}
{% assign pays_attente = 0 %}
{% for pays in site.data.countries %}
  {% if pays[1].attente > compteur attente %}
    {% assign compteur_attente = pays[1].attente %}
    {% assign pays_attente = pays %}
  {% endif %}
{% endfor %}

{% assign pays_traverses = 0 %}
{% for pays in site.data.countries %}
  {% if pays[1].attente %} {% assign pays_traverses = pays_traverses | plus:1 %} {% endif %}
{% endfor %}

<!-- Rendu -->

<div class="panel radius">
  <div class="row">
    <center><h3>Transports</h3></center>
    <div class="medium-12 large-centered columns">
      <div class="medium-4 columns"><i class="material-icons" style="font-size:18px">person_pin</i> {{ total_conducteurs }} conducteurs</div>
      <div class="medium-4 columns"></div>
      <div class="medium-4 columns"></div>
    </div>
  </div>
</div>
