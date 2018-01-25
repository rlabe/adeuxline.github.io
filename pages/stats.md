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
    {% assign total_pays = total_pays | plus: pays[1].traverse %}
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
{% for pays in site.data.countries %}
    {% assign total_distance = total_distance | plus: pays[1].distance %}
{% endfor %}

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
    <center><h3>J'ai déjà traversé {{ total_pays }} pays.</h3><br/>
    <a href="/pays/">Voir la liste</a></center>
  </div>
</div>

<div class="panel">
  <div class="row">
    <center><h3>Transports</h3></center>
    <div class="medium-12 large-centered columns">
      <div class="medium-6 columns"><i class="material-icons" style="font-size:18px">person_pin</i> {{ total_conducteurs }} conducteurs</div>
      <div class="medium-6 columns"><i class="material-icons" style="font-size:18px">near_me</i> {{ total_distance }} km</div>
    </div>
    <div class="medium-12 large-centered columns">
      <div class="medium-4 columns"><i class="material-icons" style="font-size:18px">time_to_leave</i> {{ km_voiture }} km en voiture</div>
      <div class="medium-4 columns"><i class="material-icons" style="font-size:18px">local_shipping</i> {{ km_camion }} km en camion</div>
      <div class="medium-4 columns"><i class="material-icons" style="font-size:18px">directions_boat</i> {{ km_bateau }} km en bateau</div>
    </div>
  </div>
</div>
<div class="panel">    
  <div class="row">
    <center><h3>Pour le fun</h3></center>
    <div class="medium-12 large-centered columns">
      <div class="medium-4 columns"><i class="material-icons" style="font-size:18px">local_post_office</i> {{ total_cartes }} cartes postales</div>
      <div class="medium-4 columns"><i class="material-icons" style="font-size:18px">brightness_2</i> {{ total_nuits_dehors }} nuits dehors</div>
    </div>
  </div>
</div>

