---
layout: page
show_meta: false
title: "Statistiques"
header:
   image_fullwidth: "header_roadmap_3.jpg"
permalink: "/stats/"
---

<!-- Calculs -->
{% assign total_pays = 0 %}
{% for pays in site.data.countries %}
    {% if pays.traverse %}
    {% assign sum_superficie = sum_superficie | plus: 1 %}
    {% endif %}
{% endfor %}

{% assign total_jours = 0 %}
{% for pays in site.data.countries %}
    {% assign total_jours = total_jours | plus: pays[1].jourspasses %}
{% endfor %}

{% assign total_conducteurs = 0 %}
{% for pays in site.data.countries %}
    {% assign total_conducteurs = total_conducteurs | plus: pays[1].conducteurs %}
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

{% assign totale_distance = 0 %}
{% assign totale_distance = totale_distance | plus: km_voiture %}
{% assign totale_distance = totale_distance | plus: km_camion %}
{% assign totale_distance = totale_distance | plus: km_bateau %}

{% assign total_cartes = 0 %}
{% for pays in site.data.countries %}
    {% assign total_cartes = total_cartes | plus: pays[1].cartes_postales %}
{% endfor %}

{% assign total_nuits_dehors = 0 %}
{% for pays in site.data.countries %}
    {% assign total_nuits_dehors = total_nuits_dehors | plus: pays[1].nuits_dehors %}
{% endfor %}

{% include _map_global.html %}

<!-- Rendu -->
<div class="panel">
  <div class="row">
    <center><h3>Transports</h3></center>
    <div class="medium-12 large-centered columns">
      <div class="medium-6 columns"><i class="material-icons" style="font-size:18px">person_pin</i> {{ total_conducteurs }} conducteurs</div>
      <div class="medium-6 columns"><i class="material-icons" style="font-size:18px">person_pin</i> {{ total_pays }} km</div>
    </div>
    <div class="medium-12 large-centered columns">
      <div class="medium-4 columns"><i class="material-icons" style="font-size:18px">person_pin</i> {{ km_voiture }} km en voiture</div>
      <div class="medium-4 columns"><i class="material-icons" style="font-size:18px">person_pin</i> {{ km_camion }} km en camion</div>
      <div class="medium-4 columns"><i class="material-icons" style="font-size:18px">person_pin</i> {{ km_bateau }} km en bateau</div>
    </div>
  </div>
</div>
<div class="panel">    
  <div class="row">
    <center><h3>Pour le fun</h3></center>
    <div class="medium-12 large-centered columns">
      <div class="medium-4 columns"><i class="material-icons" style="font-size:18px">person_pin</i> {{ total_cartes }} cartes postales</div>
      <div class="medium-4 columns"><i class="material-icons" style="font-size:18px">person_pin</i> {{ total_nuits_dehors }} nuits dehors</div>
    </div>
  </div>
</div>

