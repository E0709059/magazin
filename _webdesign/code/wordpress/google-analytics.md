---
layout: page
subheadline: "WordPress Rezepte"
title: "Google Analytics in WordPress Theme einbauen"
teaser: "Um das Statistik-Werkzeug Google Analytics schnell in ein WordPress Theme einzubauen, reicht das folgende Code-Schnipsel."
header:
    image: code_shutterstock_225068266.png
    background-color: "#82cbd0"
    caption: »Flat design vector concept« von Shutterstock
    caption_url: http://www.shutterstock.com/pic.mhtml?id=225068266&src=id
image:
    thumb: icon/icon-wordpress.svg
style: "#masthead-with-background-color { padding: 0; }"
categories:
    - code
tags:
    - wordpress
    - rezept
    - code
breadcrumb: true
---
Dazu fügen Sie den folgenden Code einfach in die *functions.php*-Datei des Themes ein. Anschließend müssen Sie noch Ihre Google Analytics-ID anpassen – siehe `DEINE-GOOGLE-ANALYTICS-ID`im Code.

Damit eingeloggte Nutzer nicht mitgeschnitten und in die Statistiken einbezogen werden, deaktiviert man den Aufruf von Google Analytics mit Hilfe der IF-Abfrage:

`if ( !is_user_logged_in() ) { // auszuführenden Code hier einfügen }`

Wichtig bei diesem Befehl ist das `!` vor `is_user_logged_in()`. Das `!` kehrt die IF-Abfrage um. Gelesen wird die Abfrage dann so: *Wenn **keiner** eingeloggt ist, dann füge den folgenden Code ein.*



{% highlight php startinline=true %}
<?php
//
// Google Analytics Einbau
// Die Abfrage if( !is_preview()) deaktiviert Google Analytics
// für eingeloggte Nutzer
//
add_action('wp_footer', 'ga');
function ga() {
   if ( !is_user_logged_in() ) { // Abfrage, ob Nutzer eingeloggt
?>
<script>
  (function(i,s,o,g,r,a,m){i['GoogleAnalyticsObject']=r;i[r]=i[r]||function(){
  (i[r].q=i[r].q||[]).push(arguments)},i[r].l=1*new Date();a=s.createElement(o),
  m=s.getElementsByTagName(o)[0];a.async=1;a.src=g;m.parentNode.insertBefore(a,m)
  })(window,document,'script','//www.google-analytics.com/analytics.js','ga');

  ga('create', 'DEINE-GOOGLE-ANALYTICS-ID', 'auto');
  ga('require', 'linkid', 'linkid.js');
  ga('set', 'anonymizeIp', true);
  ga('send', 'pageview');

</script>
<?php
   }
}
?>
{% endhighlight %}
