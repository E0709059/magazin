---
layout: page-fullwidth
subheadline: "Suchmaschinenoptimierung (SEO)"
title: "Die wichtigsten HTML-Befehle für die Suchmaschinenoptimierung"
meta_description: "»Suchmaschinenoptimierung Teil 3« zeigt Ihnen, wie Sie optimale Keywords (Suchworte, Schlagwörter) für Ihre Artikel recerchieren, aussuchen und nutzen."
teaser: "Generell gilt: Je spezieller die Inhalte, desto größer ist die Wahrschein&shy;lichkeit, eine gute Platzierung in den Suchmaschinen zu erreichen. Das sogenannte »Ranking« beeinflussen Sie maßgeblich, indem Sie Ihr Material sinnvoll aufarbeiten. Denn ein Dokument wird nur dann Teil eines Suchergebnisses, wenn es das gesuchte Wort als Begriff enthält.Darum gehört zu den wichtigsten Aufgaben die Wahl der geeigneten Schlüsselwörter."
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

{% include alert info='WordPress eignet sich hervorragend für die Suchmaschinenoptimierung. Die Struktur der Permalinks beeinflussen Sie im Backend in den Einstellungen unter Permalinks.' %}

Merken Sie sich auch die folgenden Richtlinien zum URLDesign:

* Benutzen Sie den Bindestrich bzw. das Minuszeichen zum Trennen von Keywords.
* Überschreiten Sie nicht eine Verzeichnistiefe von mehr als drei Unterverzeichnissen. Je weiter unten ein Dokument in der Baumstruktur angeordnet ist, desto weniger Bedeutung wird ihm beigemessen.
* Vermeiden Sie PHP-Parameterangaben in der URL, denn Zeichen wie »?« oder »&« verschlechtern das Ergebnis, weil Google diese Dokumente als dynamisch einstuft. Das bedeutet: je statischer eine Webseite, desto besser.

[Teil 5: Aufbau und Struktur einer suchmaschinenoptimierten Webseite ›]({{ site.url }}/struktur-suchmaschinenoptimierte-website/)
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
