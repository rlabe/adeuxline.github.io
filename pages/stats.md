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
    <div class="medium-4 columns">
      <ul>
        <li><i class="material-icons" style="font-size:18px">person_pin</i> {{ total_conducteurs }} conducteurs</li>
        <li><i class="material-icons" style="font-size:18px">directions_car</i> 1500 km</li>
        <li><i class="material-icons" style="font-size:18px">hourglass_empty</i> 4h30</li>
        <li><i class="material-icons" style="font-size:18px">network_check</i> 215 km/h</li>
      </ul>
    </div>
    <div class="medium-4 columns">
      <ul>
        <li><i class="material-icons" style="font-size:18px">schedule</i> 202 h</li>
        <li><i class="material-icons" style="font-size:18px">directions_railway</i> 12400 km</li>
        <li><i class="material-icons" style="font-size:18px">hourglass_empty</i> 82 h</li>
          </ul>
    </div>
    <div class="medium-4 columns">
          <ul>
        <li><i class="material-icons" style="font-size:18px">schedule</i> 72 h</li>
        <li><i class="material-icons" style="font-size:18px">directions_bus</i> 4000 km</li>
        <li><i class="material-icons" style="font-size:18px">hourglass_empty</i> 12 h</li>
          </ul>
    </div>
  </div>
</div>
<div class="panel radius">
  <div class="row">
    <center><h3>Pour le fun</h3></center>
    <div class="medium-4 columns">
          <ul>
        <li><i class="material-icons" style="font-size:18px">my_location</i> 7 villes</li>
         
          </ul>
    </div>
    <div class="medium-4 columns">
          <ul>
        <li><i class="material-icons" style="font-size:18px">local_post_office</i> 89 cartes postales</li>
          </ul>
    </div>
    <div class="medium-4 columns">
          <ul>
        <li><i class="material-icons" style="font-size:18px">brightness_2</i> 7 nuits dehors</li>
          </ul>
    </div>
  </div>
</div>

<div class="panel radius">
  <div class="row">
    <div class="medium-9 large-centered columns">
      <div class="medium-4 columns">TEST 1</div>
      <div class="medium-4 columns">TEST 2</div>
      <div class="medium-4 columns">TEST 3</div>
    </div>
  </div>
</div>