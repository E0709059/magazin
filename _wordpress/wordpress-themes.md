---
layout: page-fullwidth
subheadline: Theme
title: Herausragende WordPress Themes
teaser: "Webdesigner versorgen die WordPress-Community kontinuierlich mit neuen Layouts und Design. Von diesen Themes gibt es mittlerweile eine unüberschaubare Anzahl. Phlow Magazin stellt die herausragende Themes vor."
permalink: /wordpress/themes/
categories:
    - webdesign
tags:
    - wordpress
    - themes
image:
    thumb: icon/icon-wordpress.svg
header:
    image: icon/wordpress-logo-498x113.png
    background-color: "#82cbd0"
style: "#navigation > nav > section > ul.left > li:nth-child(5) > a { background: #82cbd0; color: #fff; }"
---
<div class="row">
<div class="large-7 columns" markdown="1">

WordPress ermöglicht, dass Sie eigene individuelle Webdesigns designen und programmieren können. Diese Möglichkeit nutzen zahlreiche Blogger und Webdesigner, um ihre individuellen Vorstellungen umzusetzen.

Angehende Blogger, die (noch) keine Ahnung von HTML, CSS und PHP haben, brauchen aber nicht auf ein eigenwilliges Layout zu verzichten. Denn zahlreiche Webdesigner veröffentlichen Ihre WordPress-Layouts, die so genannten Themes, frei und kostenlos. Wir haben eine Auswahl professioneller WordPress Themes zusammengestellt.


## Was ist eine WordPress Theme?

Eine der großartigen Funktionen von WordPress sind Themes. Themes bestimmten das Aussehen einer WordPress-Website. Ein **Theme** installiert man einfach, indem man den jeweiligen Theme-Ordner auf den Server hochlädt. Diese Theme-Ordner beinhalten so genannte Templates.

Diese **Templates** sind Schablonen, die das Aussehen der verschiedenen von WordPress ausgegebenen Webseiten bestimmen. In der Regel verfügt ein Theme immer über ein Template für die Startseite, die Artikel, die Seiten und die Archivseiten.

Worauf Sie bei der Wahl eines WordPress-Themes achten sollten, lesen Sie in unserem Artikel [»Auswahlkriterien für WordPress Themes«][3].



{% for theme in site.data.wordpress-themes %}

## {{ theme.name }}

{% for screenshot in theme.screenshots %}
<img src="{{ site.urlimg }}{{ screenshot }}" alt="WordPress Theme {{ theme.name }}">
{% endfor %}

{{ theme.description | markdownify }}


{% unless theme.pro == NULL %}
<h3>Pro</h3>
<ul class="plus">
{% for item in theme.pro %}
    <li>{{ item }}</li>
{% endfor %}
</ul>
{% endunless %}


{% unless theme.contra == NULL %}
<h3>Contra</h3>
<ul class="minus">
{% for item in theme.contra %}
    <li>{{ item }}</li>
{% endfor %}
</ul>
{% endunless %}



{% if theme.download %}<a class="button radius success" href="{{ theme.download }}">Download</a>{% endif %}
{% if theme.demo %}<a class="button radius success" href="{{ theme.demo }}">Demo</a>{% endif %}
{% if theme.anleitung %}<a class="button radius success" href="{{ theme.anleitung }}">Anleitung</a>{% endif %}

{% endfor %}



## Noch mehr WordPress Themes

Die folgenden Themes nutzt [Automattic][4], die Firma hinter WordPress, für die eigene Blogging-Plattform WordPress.com. Das garantiert hochwertige Themes, die höchstwahrscheinlich gepflegt werden und mit neuen Funktionen erweitert werden. Eine [Übersicht über alle (freien)WordPress-Themes][5] listet weitere großartige und freie Themes auf. Hier die Themes, die mir persönlich sehr zusagen:

* [Catch Everest](http://catchthemes.com/theme-instructions/catch-everest/)
* [Visual](http://themes.wptheming.com/visual/)
* [Hatch](http://alienwp.com/themes/hatch/)
* [Fresh & Clean](http://theme.wordpress.com/themes/fresh-and-clean/)
* [Quintus](http://theme.wordpress.com/themes/quintus/)
* [Sight](http://theme.wordpress.com/themes/sight/)
* [Twenty Twelve](http://theme.wordpress.com/themes/twentytwelve/)
* [Oxygen](http://theme.wordpress.com/themes/oxygen/)
* [Book Lite](http://theme.wordpress.com/themes/book-lite/)
* [Pinboard](http://www.onedesigns.com/wordpress-themes/pinboard)
* [Origin](http://wordpress.org/themes/origin)






 [1]: http://dimsemenov.com/themes/touchfolio/
 [2]: {{ site.url }}/wordpress/themes/
 [3]: {{ site.url }}/wordpress/checkliste/
 [4]: http://automattic.com/
 [5]: http://theme.wordpress.com/
 [6]: #
 [7]: #
 [8]: #
 [9]: #
 [10]: #



 </div><!-- /.large-7 -->
<div class="large-5 columns">

<div class="panel radius" markdown="1">
**Themes**
{: #toc }
*  TOC
{:toc}
</div>

{% include ad/das-wordpress-buch.html %}

</div><!-- /.large-5 -->
</div><!-- /.row -->