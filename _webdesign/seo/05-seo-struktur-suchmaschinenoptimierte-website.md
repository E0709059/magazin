---
layout: page-fullwidth
subheadline: "Suchmaschinenoptimierung (SEO)"
title: "Aufbau und Struktur einer suchmaschinenoptimierten Webseite"
teaser: "Im Folgenden erläutere ich Ihnen weitere wichtige HTML-Tags für den Aufbau eines Dokumentes. Diese Liste von Tags stammt aus einer Umfrage unter SEO-Experten, die Sie bei <a href='https://moz.com/search-ranking-factors'>Search Engine Ranking Factors</a> finden."
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
permalink: /struktur-suchmaschinenoptimierte-website/
---
<div class="row">
<div class="medium-5 medium-push-7 columns" markdown="1">
<h3 class="m0">Suchmaschinen-Special</h3>

{% include list-collection-by-tag.html collection='webdesign' tag='seo-special' limit='25' %}

</div><!-- /.medium-5.columns -->
<div class="medium-7 medium-pull-5 columns" markdown="1">


**Jede Webseite braucht eine Überschrift per `<h1>`-Tag:** Neben der Überschrift im `<title>`-Tag muss die Webseite auch eine Überschrift im `<body>`-Bereich der Webseite haben. Zuständig dafür ist das `<h1>`- Tag. Für das `<h1>`-Tag gelten die gleichen Regeln wie für das `<title>`-Tag: Je weiter vorne sich wichtige Keywords befinden, desto besser werden sie bewertet. Nutzen Sie im `<title>` als auch in der `<h1>` die gleiche Überschrift zu.

**Einen Artikel gliedert man mit `<h2>`- und `<h3>`-Tags:** Längere Artikel strukturiert man mithilfe von Zwischenüberschriften. Zwischenüberschriften helfen dem Leser beim Scannen des Texts und dienen als Orientierungspunkt beim Scrollen. Texte, die länger als 1.000 Zeichen lang sind, sollten Sie deswegen nicht nur aus SEO-Gründen mit Zwischenüberschriften versehen.

Auch in den Zwischenüberschriften platzieren Sie die gewünschten Schlagwörter, diesmal vielleicht im Plural, wenn bereits weiter vorne der Begriff im Singular verwendet wurde. Mal vorne, mal hinten. Wie bei den URLs gilt: Finger weg vom so genannten *Keyword-Stuffing*! Übertreiben Sie es nicht und vergraulen Sie nicht Ihre Leser durch übermäßige Wiederholungen.

**Bilder *beschriftet* man mit Schlüsselworten im Dateinamen und mittels des Alt-Attributs:** Noch können Suchmaschinen Bilder nicht analysieren und feststellen, was auf einem Bild zu sehen ist. Vielleicht ist auch dies eines Tages möglich, aber bis dahin dauert es sicherlich noch ein wenig. Darum lesen Suchmaschinen wie auch Browser für Blinde den Namen und die Bezeichnung des Bildes aus.

Sie sehen, hier ist die Suchmaschinenoptimierung nicht nur Suchmaschinen&shy;marketing, sondern verbessert Ihre Webseite auch direkt für den Besucher. Obendrein zeigt ein Browser bei einem verloren gegangenen Bild eine Beschreibung an. Geben Sie darum Ihren Bildern aussagekräftige Namen, in denen die Keywords ein weiteres Mal auftauchen, und betiteln Sie Ihre Bilder mithilfe des `alt`- und `title`-Attributs. Optimal sieht das dann so aus:

{% highlight html %}
<img src="tipps-tricks-twitter.jpg" alt="Tipps und Tricks für Twitter"
title="Tipps und Tricks für Twitter" height="276" width="597"/>
{% endhighlight %}

**Heben Sie Schlagworte und Begriffe mit `<em>` und `<strong>` hervor:** Ein weiteres hilfreiches Stilmittel, um Texte zu gestalten, die schnell erfassbar sind, ist die Methode fette Schrift zu nutzen. Exzellent nutzt zum Beispiel das englischsprachige Smashing Magazine – *sowieso eine tolle Adresse für Webdesigntipps* – diese Textauszeichnung – unter anderem in diesem Artikel: [»Getting Started With Content Management Systems«][7].


[Teil 6: Links richtig setzen ›]({{ site.url }}/links-setzen/)
{: .button.radius }



 [1]: http://de.wikipedia.org/wiki/Braillezeile
 [2]: {{ site.url }}/recherche/
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
