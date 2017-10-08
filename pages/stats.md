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
- Superficie totale: {{ sum_superficie }}
