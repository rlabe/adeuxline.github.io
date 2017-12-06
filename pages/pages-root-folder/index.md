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
  url: '/article/pourquoi-le-stop/'
  image: widget1.jpg
  text: "Le stop permet de voyager à moindre coût, de faire des rencontres insolites de de découvrir la culture locale."
widget2:
  title: "L&apos;école primaire"
  url: '/article/partenariat-ecole-chapelle-aux-champs/'
  image: widget2.png
  text: "Grâce au soutien des enseignants, les enfants pourront découvrir et parcourir le monde avec moi."
widget3:
  title: "L&apos;hôpital Reine Fabiola"
  url: '/article/partenariat-hopital-reine-fabiola/'
  image: widget3.png
  text: "La mascotte de l&apos;hôpital m'accompagnera pendant tout le trajet et visitera les endroits insolites du monde."
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
