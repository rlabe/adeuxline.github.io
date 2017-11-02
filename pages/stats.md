---
layout: page
show_meta: false
title: "Statistiques"
subheadline: "Quelques stats"
teaser: "Quelques chiffres..."
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


<!-- Rendu -->
Nous sommes partis le {{ "Jul 28, 2017" | date: "%e %B %Y" }} et nous sommes revenus le {{ "Aug 31, 2017" | date: "%e %B %Y" }}.



- Conducteurs rencontrés: 7
- Km parcourus:
  * en voiture: 1500
  * en train: 12400
  * en bus : 4000


- Villes visitées: 7
- Attente la plus longue: 4h30
- Distance maximum dans le même véhicule sur route: 700km (Rosenheim - Budapest)
- Vitesse maximum atteinte: 215km/h (Kai)
- Temps passé dans un train: 202h
- Temps maximum passé dans le même train: 82h (Moscou - Oulan-Oudé)
- Temps passé dans un bus: 72h
- Temps maximum passé dans le même bus: 12h (Oulan-Bator - Oulan-Oude)
- Cartes postales envoyées: 89
- Nuits dehors: 5
