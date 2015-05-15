---
layout: page-fullwidth
subheadline: "Suchmaschinenoptimierung (SEO)"
title: "Links richtig setzen"
teaser: "Findet der Webcrawler einen Link auf einer Webseite, ist der Suchmaschine in der Regel erst einmal nicht klar, worum es sich bei der verlinkten Webseite handelt. Außerdem weiß die Suchmaschine nicht, ob es sich um eine Linkempfehlung handelt. Darum analysiert die Suchmaschine den Text des Links und die Linkattribute. Anschließend vergleicht die Maschine die verlinkte Webseite mit dem Linktext."
image:
    thumb: seo-thumb.jpg
header:
    image: seo-suchmaschinenoptimierung-shutterstock_227734471.png
    background-color: "#56b8d1"
    caption: "»Flat web illustration infographics« von Shutterstock"
    caption_url: http://www.shutterstock.com/pic.mhtml?id=227734471&src=id
style: "#masthead-with-background-color > div > figure { text-align: center; }"
categories:
    - webdesign
tags:
    - artikel
    - seo-special
    - suchmaschinenoptimierung
    - struktur
    - website
    - seo
permalink: /links-setzen/
---
<div class="row">
<div class="medium-5 medium-push-7 columns" markdown="1">
<h3 class="m0">Suchmaschinen-Special</h3>

{% include list-collection-by-tag.html collection='webdesign' tag='seo-special' limit='25' %}

</div><!-- /.medium-5.columns -->
<div class="medium-7 medium-pull-5 columns" markdown="1">

<div class="panel radius" markdown="1">
Inhalt
{: #toc }
*  TOC
{:toc}
</div>

Ein Beispiel: Wenn man eine externe oder interne Webseite verlinkt, vermeidet man am besten aussagelose Begriffe wie »hier«, »weiterlesen« oder »mehr«. Verlinkt man zum Beispiel einen Interview-Podcast, sollte mindestens einer der beiden Begriffe *Interview* oder *Podcast* im Linktext auftauchen. Findet die Suchmaschine im nächsten Schritt auch noch die gleichen Wörter auf der verlinkten Webseite, wird diese mit hoher Wahrscheinlichkeit zu einem oder beiden Keywords indexiert.

Das bedeutet, dass es wichtiger für Ihre Webseite ist, wenn sie jemand mit guten Keywords im Linktext verlinkt als z.B. mit unbedeutenden Wörtern oder Eigennamen.



## Perfekte Text-Links

Ein Beispiel: Jeannette Corneille arbeitet als Grafik-Designerin und eine Kollegin verlinkt Sie in einem Artikel. Auch wenn die folgende Verlinkung offensichtlich ist, handelt es sich bei der zweiten Variante um eine bessere Verlinkung, da zwei Schlüsselbegriffe mit der verlinkten Website assoziiert werden:

Gut:

{% highlight html %}
<a href="http://jcorneille.de">Jeannette Corneille</a> bietet Grafik-Design in Köln an.
{% endhighlight %}

Besser:

{% highlight html %}
Auf Ihrer Website zeigt Jeannette Corneille <a href="http://jcorneille.de">ihre Grafik-Design-Arbeiten</a> und...
{% endhighlight %}

Perfekt:

{% highlight html %}
Auf Ihrer Website zeigt Jeannette Corneille <a href="http://jcorneille.de" title="Grafik Design in Köln von Jeannette Corneille">ihre Grafik-Design-Arbeiten</a> und...
{% endhighlight %}



## Optimierte Bilder-Links

Nutzen Sie Bilder als Links – z.B. verlinkte Bilder in einem Beitrag –, hilft  das Universalattribut `title="Keywords"` bei der Suchmaschinenoptimierung. Dieses können Sie sowohl im `<a>`-Tag als auch im `<img>`-Tag verwenden. Das sieht dann so aus:

{% highlight html %}
<a title="Kunden und Netzwerk" href="http://link.de/kunden.html">
<img src="navigation_kunden_netzwerk.gif" alt="Kunden und Netzwerk"
title="Kunden und Netzwerk"></a>
{% endhighlight %}

Aber auch auf Ihrer eigenen Website hilft eine gute interne Verlinkung den Suchmaschinen und erleichtert diesen, Ihre Webseite thematisch einzuordnen. Wächst der Umfang Ihrer Website, unterstützt die intelligente Strukturierung der Inhalte durch eine durchdachte interne Verlinkung das Ranking in den Suchmaschinen. Bauen Sie Link-Strukturen mit Hilfe von Textlinks auf, in welchen Sie die Schlagwörter unterbringen.

Ein weiterer wichtiger Faktor für die Anerkennung einer Website sind korrekte Links. Prüfen Sie Ihre Seite darum regelmäßig auf defekte Links. Sowohl Besucher als auch Suchmaschinen-Crawler werden Ihrer Seite schnell den Rücken kehren, wenn die Anzahl defekter Links überhand nimmt.

{% include alert info='Für WordPress empfehle ich Ihnen das <a href="http://magazin.phlow.de/wordpress/plugins/#kaputte-links-finden-reparieren-und-lschen">Plug-in Broken Link Checker</a>. Dieses untersucht automatisch Ihre Links in Artikeln auf Aktualität.' %}

Vermeiden Sie auch, Links mithilfe von JavaScript zu setzen. Diese Links entdecken Suchmaschinen womöglich nicht oder bewerten sie geringer. Links in Flash kann eine Suchmaschine überhaupt nicht erkennen und weiterverfolgen. Aber die Verwendung von Flash ist dank moderner Browser-Technologie glücklicherweise eine veraltete Technik.



## Die Linkattribute nofollow und follow

Wie aber verlinke ich eine Webseite, die thematisch für meinen Beitrag wichtig ist, deren Inhalte ich aber nicht in den Suchmaschinen »promoten« möchte? Stellen Sie sich vor, Sie schreiben einen Artikel über Rechtsextremismus. In diesem Artikel möchten Sie eine Webseite von Nazis verlinken, jedoch nicht deren Sichtbarkeit in Suchmaschinen unterstützen.

Für diese Art von Links haben sich die Suchmaschinenbetreiber die beiden Linkattribute `nofollow` und `follow` ausgedacht. Während `follow` eigentlich  obsolet ist, weil man mit einem normalen Link eine Empfehlung ausspricht, so spricht man **mit `nofollow` explizit keine Empfehlung** aus.

{% highlight html %}
<a href="http://bloeder-nazi.de" rel=“nofollow“>Nazi-Seite</a>
{% endhighlight %}


[Teil 7: Programme und Services für die Suchmaschinenoptimierung ›]({{ site.url }}/programme-services-suchmaschinenoptimierung//)
{: .button.radius }


 [1]: http://de.wikipedia.org/wiki/Braillezeile
 [2]: {{ site.url }}/recherche/
 [3]: https://adwords.google.de/KeywordPlanner
 [4]: https://www.google.de/adwords/
 [5]: https://metager.de/klassik/asso/
 [6]: https://moz.com/search-ranking-factors
 [7]: http://www.smashingmagazine.com/2009/11/08/getting-started-with-content-management-systems/
 [8]: https://validator.w3.org/
 [9]: #
 [10]: #

</div><!-- /.medium-7.columns -->
</div><!-- /.row -->
