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
  text: "Le stop permet de développer différentes thématiques:<br/>1. Le côté économique<br/>2. Le côté social<br/>3. Le côté écologique<br/>4. Le facteur humain"
widget2:
  title: "L'école primaire"
  url: 'http://adeuxline.github.io/'
  text: "Grâce au soutien des enseignants, les enfants pourront découvrir et parcourir le monde avec moi."
  video: '<a href="#" data-reveal-id="videoModal"><img src="http://phlow.github.io/feeling-responsive/images/start-video-feeling-responsive-302x182.jpg" width="302" height="182" alt=""/></a>'
widget3:
  title: "L'hôpital Reine Fabiola"
  url: 'https://adeuxline.github.io/voyage/transsiberien/'
  image: transsiberien_01.JPG
  text: "La mascotte de l'hôpital m'accompagnera pendant tout le trajet et visitera les endroits insolites du monde."
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
