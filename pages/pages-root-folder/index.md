---
#
# Use the widgets beneath and the content will be
# inserted automagically in the webpage. To make
# this work, you have to use › layout: frontpage
#
layout: frontpage
header:
  image_fullwidth: header-bus.jpg

widget1:
  title: "Pourquoi le stop ?"
  url: 'http://adeuxline.github.io/about/'
  image: widget-1-302x182.jpg
  text: 'Le stop permet de voyager à moindre coût, de faire des rencontres et de découvrir de la culture locale plus facilement.'
widget2:
  title: "Les monnaies locales"
  url: 'http://adeuxline.github.io/'
  text: 'Les <em>monnaies locales</em> sont une alternative économique intéressante à découvrir à travers le monde.'
  video: '<a href="#" data-reveal-id="videoModal"><img src="http://phlow.github.io/feeling-responsive/images/start-video-feeling-responsive-302x182.jpg" width="302" height="182" alt=""/></a>'
widget3:
  title: "Le transsiberien"
  url: 'https://adeuxline.github.io/voyage/transsiberien/'
  image: transsiberien_01.JPG
  text: 'Plus de 200h de train à travers la Hongrie, l&#39;Ukraine et la Russie... Un long voyage !'
# Use the call for action to show a button on the frontpage
#
# To make internal links, just use a permalink like this
# url: /getting-started/
#
# To style the button in different colors, use no value
# to use the main color or success, alert or secondary.
# To change colors see sass/_01_settings_colors.scss
#
callforaction:
  url: https://adeuxline.github.io/newsletter/
  text: S'abonner à la newsletter
  style: alert
permalink: /index.html
#
# This is a nasty hack to make the navigation highlight
# this page as active in the topbar navigation
#
homepage: true
---
