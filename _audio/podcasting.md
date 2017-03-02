---
layout: page-fullwidth
subheadline: "Tipps, Tricks und Quellen für die Podcast-Produktion"
title: "Podcasting: Software & Websites"
teaser: ""
permalink:
image:
    thumb: icon/icon-rss-podcast.png
header: no
---
<div class="row">
<div class="medium-5 medium-push-7 columns" markdown="1">
<div class="panel radius" markdown="1">
Inhalt
{: #toc }
*  TOC
{:toc}
</div>
</div><!-- /.medium-5.columns -->

<div class="medium-7 medium-pull-5 columns" markdown="1">


## Was ist Podcasting?

Ganz ähnlich wie der Beriff »Weblog« ist auch »Podcast« eine Wortneuschöpfung: Dieses Kunstwort setzt sich aus den Wörtern »iPod«, dem MP3-Player von Apple, und »broadcast«, dem englischen Wort für Sendung, zusammen. Podcasting gilt für viele als die neue Generation des Radios, denn man könnte es als eine Art zeitver­setztes Radiohören bezeichnen.

Beim Podcasting werden Sendungen nicht live übertragen, sondern sie liegen zum Download auf einem Server abrufbereit vor. Auf diese Weise lassen sich einzelne Sendungen (auch *Episoden* genannt) problem­los downloaden und auf einen MP3-Player übertragen, so dass man sie immer mit sich trägt und genau dann hört, wenn man will. Podcast-Beiträge benutzen in der Regel die MP3-Technik.



## Podcast: Flexibler Radiohören

Der Vorteil gegenüber dem Radio liegt auf der Hand: Einen Podcast kann man nach dem Download nach Belieben vor- und zurückspulen oder einfach abbrechen, um zur nächsten Folge zu springen. Ein weiterer Vorteil ist die Tatsache, dass ein Podcast zu einem selbst bestimmten Zeitpunkt angehört werden kann – so oft man möchte. Dieser flexible Umgang unterscheidet Podcasting vom normalen Radio.

Besonders wertvoll ist die Eigenschaft, dass man bei normalen Podcasts im Archiv zurückwan­dern kann. Gefällt einem z.B. die aktuelle Folge von »Schlaflos in München«, kann man sich auch die bereits zurückliegenden Beiträge anhören. Ein weiterer Vorteil gegenüber dem Radio bilden Nischensendungen. Wo im alltäglichen Radio Nach­richten aus Subkulturen und kleinen Szenen fehlen, ermöglichen Podcasts die Berichterstattung selbst aus den kleinsten Nischen. Kein Wunder also, dass man in der immer größer werdenden Podcast-Welt so gut wie jedes Thema findet.

Ein Podcast selbst ist dabei nichts anderes als ein [RSS][1]-Feed der Version 2.0. RSS ist ein auf XML basierendes Dateiformat für die Verbreitung von Webinhalten, auch »Syndication« oder auf Neudeutsch »Syndizierung« genannt. In der Regel transpor­tieren RSS-Feeds Newsticker-Daten wie Artikelüberschrift, Anreißer und Link zum gesamten Artikel. Feeds werden meistens von News-Aggregatoren ausgelesen und für den Leser visuell aufbereitet. RSS-Feeds lassen sich aber auch als Newsticker in die eigene Website einbauen. Zahlreiche Online-Services nut­zen diese Möglichkeiten und bieten ihren Benutzern einen Service an, der RSS-Feeds in Form von Webseiten im Browser anzeigt.



## Das <enclosure>-Tag

Damit ein Podcast funktioniert, macht man sich das `<enclosure>`-Tag zunutze, das Dave Winer in seiner RSS 2.0-Spezifikation integriert hat. Mit Hilfe des `<enclosure>`-Tags können RSS-Feeds zusätzliche Links zu Medientypen wie Audiodaten, Video­daten oder Ähnlichem mitliefern. Auch wenn Podcasts in der Regel Links zu Audio­daten liefern, könnte ein Podcast z.B. auch als Abonnement für Videoclips dienen. In einem solchen Fall bezeichnet man dann den ursprünglichen Podcast als »Video­cast«.

Der Begriff »Abonnement« im Zusammenhang mit Podcasts ist zuweilen etwas missverständlich. Natürlich handelt es sich hier nicht um ein Dauerschuldverhältnis wie etwa bei einem Zeitschriftenabon­nement, das zu immer wiederkehrenden Zahlungen verpflichtet und mit einer bestimmten Frist gekündigt werden muss. Wer einen Pod­cast abonniert, erhält damit automatisch neue Episoden, schließt aber keinen Vertrag.

Um einen Podcast zu empfangen, benötigt der Benutzer eine [Podcatcher-Software][2] (z.B. iTunes). Diese wertet den abonnierten RSS-Feed aus und lädt auf Wunsch automatisch die darin verlinkte Mediendatei aus dem Internet herunter. Die meisten Podcatcher greifen Besitzern von iPods unter die Arme und importieren die Audiodateien gleich nach iTunes, von wo aus sie auf den iPod kopiert werden können.

Wie die meisten Weblog-Systeme generiert auch [WordPress][3] automa­tisch RSS-Feeds. WordPress eignet sich darum hervorragend dazu, eigene Podcasts zu veröffentlichen, da das Redaktionssystem den Benutzer unterstützt.




## Podcasting Software

### Software für die Podcast-Produktion

* [Audacity][4] - kostenloser, betriebssystemunabhängige Audioeditor für Windows, Mac, Linux
* MP3-Codec für Audacity: lame_enc ([Download bei Chip.de][5] oder [Google-Suche nach lame_enc][6]


###  Podcast-Software für den Empfang

- [iTunes](https://www.apple.com/de/itunes/)


### RSS-Podcast Generatoren

- [Podcast Generator](http://www.podcastgenerator.net/)
- [RSS-Validator](http://feedvalidator.org/)
- [Jekyll Powered Podcast XML Generator](https://github.com/DevTips/Jekyll-Powered-Podcast-XML-Generator)


## Podcasting Links

### Deutsche Podcast-Websites und Verzeichnisse

- [www.podcast.de](http://www.podcast.de/)
- [www.podster.de](http://podster.de/)
- [wiki.podcast.de](http://wiki.podcast.de/Hauptseite)


### Englische Podcast-Websites und Verzeichnisse

[www.podcastdirectory.com](http://www.podcastdirectory.com/)



</div><!-- /.medium-7.columns -->
</div><!-- /.row -->


 [1]: {{ site.url }}/video/rss/
 [2]: {{ site.url }}#podcast-software-und-podcatcher
 [3]: {{ site.url }}/wordpress/
 [4]: http://www.audacityteam.org/
 [5]: http://www.chip.de/downloads/LAME_13003295.html
 [6]: http://www.google.de/search?q=lame_enc
