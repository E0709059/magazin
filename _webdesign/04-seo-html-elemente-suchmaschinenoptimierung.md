---
layout: page-fullwidth
subheadline: "Suchmaschinenoptimierung (SEO)"
title: "Die wichtigsten HTML-Befehle für die Suchmaschinenoptimierung"
meta_description: "»Suchmaschinenoptimierung Teil 3« zeigt Ihnen, wie Sie optimale Keywords (Suchworte, Schlagwörter) für Ihre Artikel recerchieren, aussuchen und nutzen."
teaser: "Generell gilt: Je spezieller die Inhalte, desto größer ist die Wahrschein&shy;lichkeit, eine gute Platzierung in den Suchmaschinen zu erreichen. Das sogenannte »Ranking« beeinflussen Sie maßgeblich, indem Sie Ihr Material sinnvoll aufarbeiten. Denn ein Dokument wird nur dann Teil eines Suchergebnisses, wenn es das gesuchte Wort als Begriff enthält.Darum gehört zu den wichtigsten Aufgaben die Wahl der geeigneten Schlüsselwörter."
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
    - html befehle
    - seo
permalink: /html-elemente-suchmaschinenoptimierung/
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

*Onsite-Optimierung* bezeichnet das Tuning am eigenen HTML-Code sowie die Aufwertung der Seiteninhalte. Im ersten Schritt sorgt man dafür, dass der Code intakt ist. Darum bauen Sie Ihre Website nach den üblichen Webstandards auf und strukturieren Sie den Code logisch: wichtige Inhalte müssen nach vorne gezogen werden, z.B. die Überschrift.

Wenn Sie sich nicht sicher sind, ob Ihr Quellcode korrekt ist, überprüfen Sie ihn mit einem Onlinetool, z.B. mit dem [W3C Markup Validation Service][8], oder benutzen Sie für Firefox die hervorragende Erweiterung HTML-Validator. Ich kann Letztere sehr empfehlen.

<figure>
<img src="{{ site.urlimg }}suchmaschinenoptimierung-html-optimieren.png" alt="Suchmaschinenoptimierung HTML überprüfen">
<figcaption>Die HTML-Code-Qualität prüft man einfach mit dem W3C Markup Validation Service</figcaption>
</figure>

Wie ein Buch, ein Dossier oder Ähnliches hat auch eine Webseite einen einheitlichen Aufbau. Dieser unterscheidet sich kaum von den oben genannten Formaten. Auch eine Webseite braucht einen Titel, eine inhaltliche Kurzbeschreibung und einen Ort – hier die URL –, an dem man das Dokument findet.


### Die drei wichtigsten Elemente einer Webseite für die Suchmaschinen&shy;optimierung

**`<title>` – Jedes Dokument braucht eine Überschrift:** Wie bei einem normalen, journalistisch einwandfreien Artikel, ist auch bei einer Webseite die Überschrift ein maßgeblicher Faktor dafür, ob sie angeschaut wird. Denken Sie daran, dass die Überschrift nicht nur auf Ihrer Website auftaucht. Auch in RSS-Readern, in Bookmarks oder anderen Websites taucht dieser Titel auf.

![]({{ site.urlimg }}suchmaschinenoptimierung-html-befehl-2.png)

Im Vergleich zum Printmedium richtet sich die Überschrift aber nicht nur an den Leser, sondern auch an eine »dumme« Maschine, die lediglich auf Algorithmen basiert. Während ein Leser »Prinz Poldi« in Beziehung zu »Lukas Podolski« setzt, verbindet bzw. assoziert die Suchmaschine einen derartigen Artikel nicht unbedingt mit dem Fußballspieler, es sei denn, die Suchmaschine hat nach zahlreichen Links einen Zusammenhang erkannt.

Sucht jemand z.B. »Lukas Podolski«, listet die Suchmaschine nicht automatisch einen passenden Artikel wie »Prinz Poldi« auf, sondern nur dann, wenn die Keywords »Lukas Podolski« kontinuierlich im Artikel auftauchen.

Darum ist es ratsam, die primär wichtigen Keywords im Titel zu nennen. Diese Wörter positionieren Sie eingerahmt durch das `<title>`-Tag eines HTML-Dokuments, auf das die Suchmaschinen für Ihre Suchergebnisse zurückgreifen. Verschwenden Sie dabei nicht zu viele Zeichen für den Namen Ihres Weblogs bzw. Ihrer Website. Auch auf einen Slogan sollten Sie verzichten, wenn er nicht wirklich wichtige Keywords enthält, die in jedem Dokument auftauchen sollen. Hier ein Beispiel:

{% highlight html %}
<title>»Lukas Podolski: Prinz Poldi auf dem falschen Fuß erwischt«</title>
{% endhighlight %}

Wenn möglich, sollte der Titel kurz und knackig sein und nur wenige Keywords und Wörter beinhalten. Auf den Punkt getextete Überschriften helfen auch dem Leser bei der Suche, während er Inhalte überfliegt. Benutzen Sie am besten maximal 70 Zeichen, denn dadurch verhindern Sie, dass Google Ihre Überschrift selbst kürzt.

{% include alert info='Bei der Eingabe eines neuen WordPress-Artikels können Sie sowohl den Titel des Dokuments als auch die URL nach Ihren Vorlieben gestalten. Dabei setzt sich der Inhalt zwischen den &lt;title&gt;-Tags eines einzelnen Dokuments in der Regel aus dem Namen des Blogs, der Kategorie und dem Artikelnamen zusammen.<br><br>Wie und in welcher Reihenfolge die »Zutaten« angezeigt werden, hängt vom jeweiligen Theme ab. Um den Namen der URL zu ändern, müssen Sie den Artikel mindestens einmal abgespeichert haben. Dann wird der Button Bearbeiten eingeblendet, wie in Abbildung 7-6 zu sehen ist. Über einen Klick auf den Button erhalten Sie die Möglichkeit, die URL zu gestalten.' %}

![]({{ site.urlimg }}suchmaschinenoptimierung-html-befehl-1.png)

**`<meta name=»description«/>-Description:` Neben einem exzellenten Titel liegt die große Kunst darin, eine packende und überzeugende Kurzbeschreibung des auf der Webseite angebotenen Inhalts zu verfassen.** Dafür stehen Ihnen 150 bis maximal 160 Zeichen zur Verfügung. Diese Kurzbeschreibung muss Leser zum Klicken animieren, muss die wichtigsten Keywords beinhalten und auch noch gut klingen. Obendrein positioniert man auch noch die Keywords so weit vorn im Text wie möglich.

Aber gerade diese Herausforderungen machen die Suchmaschinenoptimierung spannend und verbessern oftmals Ihre Schreibfähigkeiten. Sie werden einfach gezwungen, so schnell wie möglich auf den Punkt zu kommen – eine der wichtigsten Regeln im Journalismus. Haben Sie die Kurzbeschreibung getextet, muss diese im Description-Metatag auftauchen.

{% highlight html %}
<meta name="description" content="Jeannette Corneille (Köln) bietet Kommunikation und Design mit den Schwerpunkten Illustration auf und mit Stoff, Collagen und Zeichnungen." />
{% endhighlight %}

Gleichzeitig empfehle ich, diese Kurzbeschreibung nicht nur in den Metadaten der Webseite auftauchen zu lassen, sondern auch so weit wie möglich vorn im Artikel, z.B. als Anreißer. So »sieht« die Suchmaschine, dass die Kurzbeschreibung in den Metadaten und auf der Webseite auftauchen und kein Spamming vorliegt. Je konsistenter Ihre Artikel sind, desto besser.

**`URL-Design` – lesbare, suchmaschinenfreundliche URLs:** Das letzte und nicht zu unterschätzende Element ist die URL eines Artikels. Beobachten Sie sich einmal selbst, wenn Sie Inhalte per Google & Co. suchen. Oftmals unbewusst oder mit einem kurzen Blick überprüfen Sie als Suchender die URL. Kenne ich bereits die Website? Welche Begriffe tauchen in der URL auf? Ist die URL verständlich und logisch aufgebaut?

Platzieren Sie die gleichen Keywords darum auch im Dateinamen oder der URL des Dokuments und achten Sie auf eine sinnvolle Baumstruktur Ihrer Website. Diese Struktur sollte den Aufbau Ihrer Website widerspiegeln. Vertraut Google Ihrer Website, ersetzt die Suchmaschine Links mittlerweile auch durch eine eigens generierte Breadcrumb-Navigation. So klicken Surfer sicherlich eher auf einen verständlichen als auf einen ominösen Link, der aus einer wirren Kombination von Zeichen besteht. Aussagelos wäre beispielsweise ein solcher Link:

`http://www.domain.de/arc/item=023759`

Ansprechender und sinnvoller ist der folgende Link zum gleichen
Inhalt:

`http://www.domain.de/biografie/journalist-mustermann.html`

Vermeiden Sie Übertreibungen – das sogenannte Keyword-Stuffing.Dieses werten Suchmaschinen möglicherweise als Spam-Versuch:

`http://www.domain.de/biografie/biografie/biografie-journalistmustermann.html`

{% include alert terminal='WordPress eignet sich hervorragend für die Suchmaschinenoptimierung. Die Struktur der Permalinks beeinflussen Sie im Backend in den Einstellungen unter Permalinks.' %}

Merken Sie sich auch die folgenden Richtlinien zum URLDesign:

* Benutzen Sie den Bindestrich bzw. das Minuszeichen zum Trennen von Keywords.
* Überschreiten Sie nicht eine Verzeichnistiefe von mehr als drei Unterverzeichnissen. Je weiter unten ein Dokument in der Baumstruktur angeordnet ist, desto weniger Bedeutung wird ihm beigemessen.
* Vermeiden Sie PHP-Parameterangaben in der URL, denn Zeichen wie »?« oder »&« verschlechtern das Ergebnis, weil Google diese Dokumente als dynamisch einstuft. Das bedeutet: je statischer eine Webseite, desto besser.


## Aufbau und Struktur einer suchmaschinenoptimierten Webseite

Im Folgenden erläutere ich Ihnen weitere wichtige HTML-Tags für den Aufbau eines Dokumentes. Diese Liste von Tags stammt aus einer Umfrage unter SEO-Experten, die Sie bei [Search Engine Ranking Factors][6] finden.

**Jede Webseite braucht eine Überschrift per `<h1>`-Tag:** Neben der Überschrift im `<title>`-Tag muss die Webseite auch eine Überschrift im `<body>`-Bereich der Webseite haben. Zuständig dafür ist das `<h1>`- Tag. Für das `<h1>`-Tag gelten die gleichen Regeln wie für das `<title>`-Tag: Je weiter vorne sich wichtige Keywords befinden, desto besser werden sie bewertet. Empfehlenswert ist es, sowohl im `<title>` als auch in der `<h1>` die gleiche Überschrift zu nutzen.

**`<h2>`- und `<h3>`-Tags:** Längere Artikel strukturiert man mithilfe von Zwischenüberschriften. Zwischenüberschriften helfen dem Leser beim Scannen des Texts und dienen als Orientierungspunkt beim Scrollen. Texte, die länger als 1.000 Zeichen lang sind, sollten Sie deswegen nicht nur aus SEO-Gründen mit Zwischenüberschriften versehen. Auch hier platzieren Sie die gewünschten Schlagwörter, diesmal vielleicht im Plural, wenn bereits weiter vorne der Begriff im Singular verwendet wurde. Mal vorne, mal hinten. Wie bei den URLs gilt: Finger weg vom Keyword-Stuffing! Und vergraulen Sie nicht Ihre Leser.

**Keyword Use in Alt-Tags und Bildtiteln benutzen:** Noch können Suchmaschinen Bilder nicht analysieren und feststellen, was auf einem Bild zu sehen ist. Vielleicht ist auch dies eines Tages möglich, aber bis dahin dauert es sicherlich noch ein wenig. Darum lesen Suchmaschinen wie auch Browser für Blinde den Namen und die Bezeichnung des Bilds aus. Sie sehen, hier ist die Suchmaschinenoptimierung nicht nur Suchmaschinenmarketing, sondern verbessert Ihre Webseite auch direkt für den Besucher der Site. Obendrein zeigt ein Browser bei einem verloren gegangenen Bild eine Beschreibung an. Geben Sie darum Ihren Bildern aussagekräftige Namen, in denen die Keywords ein weiteres Mal auftauchen, und betiteln Sie Ihre Bilder mithilfe des alt- und title-Attributs. Optimal sieht das dann so aus:

{% highlight html %}
<img src="twitter-robot-automaton.jpg" alt="twitter-robot-automaton"
title="twitter-robot-automaton" height="276" width="597"/>
{% endhighlight %}

**`<em>` und `<strong>`-Schlagworte fett und kursiv schreiben:** Ein weiteres
hilfreiches Stilmittel, um Texte zu gestalten, die schnell erfassbar sind, ist die Methode fette Schrift zu nutzen. Exzellent nutzt zum Beispiel das englischsprachige Smashing Magazine – *sowieso eine tolle Adresse für Webdesigntipps* – diese Textauszeichnung – unter anderem in diesem Artikel: [»Getting Started With Content Management Systems«][7].

Wie Sie sehen, lesen Sie schon anhand der URL, worum es sich in diesem Artikel handelt.



## Links richtig setzen

Findet der Webcrawler einen Link auf einer Webseite, ist der Suchmaschine in der Regel erst einmal nicht klar, worum es sich bei der verlinkten Webseite handelt. Außerdem weiß die Suchmaschine nicht, ob es sich um eine Linkempfehlung handelt. Darum analysiert die Suchmaschine den Text des Links und die Linkattribute. Anschließend vergleicht die Maschine die verlinkte Webseite mit dem Linktext. Ein Beispiel:

Wenn man eine externe oder interne Webseite verlinkt, vermeidet man am besten aussagelose Begriffe wie »hier«, »weiterlesen« oder »mehr«. Verlinkt man zum Beispiel einen Interview-Podcast, sollte mindestens einer der beiden Begriffe im Linktext auftauchen. Findet die Suchmaschine im nächsten Schritt auch noch die gleichen Wörter auf der jeweiligen Webseite, wird diese mit hoher Wahrscheinlichkeit zu diesen beiden Keywords indexiert.

Das bedeutet, dass es wichtiger für Ihre Webseite ist, wenn sie jemand mit guten Keywords im Linktext verlinkt als z.B. mit unbedeutenden Wörtern oder Eigennamen.

Werden Bilder als Links benutzt – z.B. in einer Navigation –, nutzt man das Universalattribut `title="Keywords"` sowohl im Link-Tag als auch im `<img>`-Tag. Das sieht dann so aus:

{% highlight html %}
<a title="Kunden und Netzwerk" href="http://link.de/kunden.html">
<img src="navigation_kunden_netzwerk.gif" alt="Kunden und Netzwerk"
title="Kunden und Netzwerk" /></a>
{% endhighlight %}

Aber auch auf Ihrer eigenen Website hilft eine gute interne Verlinkung den Suchmaschinen und erleichtert diesen, Ihre Webseite thematisch einzuordnen. Wächst der Umfang Ihrer Website, unterstützt die Ausgestaltung einer internen Verlinkung das Ranking in den Suchmaschinen.

Ein weiterer wichtiger Faktor für die Anerkennung einer Website sind korrekte Links. Prüfen Sie Ihre Seite darum regelmäßig auf defekte Links. Sowohl Besucher als auch Suchmaschinen-Crawler werden Ihrer Seite schnell den Rücken kehren, wenn die Anzahl defekter Links überhandnimmt.

{% include alert info='Für WordPress empfehle ich Ihnen das <a href="http://magazin.phlow.de/wordpress/plugins/#kaputte-links-finden-reparieren-und-lschen">Plug-in Broken Link Checker</a>. Dieses untersucht automatisch Ihre Links in Artikeln auf Aktualität.' %}

Vermeiden Sie es auch, Links mithilfe von JavaScript zu setzen. Diese Links entdecken Suchmaschinen womöglich nicht oder bewerten sie geringer. Links in Flash kann eine Suchmaschine überhaupt nicht erkennen und weiterverfolgen.


### Die Linkattribute nofollow und follow

Wie aber verlinke ich eine Webseite, die thematisch für meinen Beitrag wichtig ist, deren Inhalte ich aber nicht in den Suchmaschinen »promoten« möchte? Stellen Sie sich vor, Sie schreiben einen Artikel über Rechtsextremismus. In diesem Artikel möchten Sie eine Webseite von Nazis verlinken, jedoch nicht deren Sichtbarkeit in Suchmaschinen unterstützen.

Für diese Art von Links haben sich die Suchmaschinenbetreiber die beiden Linkattribute `nofollow` und `follow` ausgedacht. Während `follow` eigentlich  obsolet ist, weil man mit einem normalen Link eine Empfehlung ausspricht, so spricht man **mit `nofollow` explizit keine Empfehlung** aus.

{% highlight html %}
<a href="http://bloeder-nazi.de" rel=“nofollow“>Nazi-Seite</a>
{% endhighlight %}



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
