---
layout: page
title:  "YAML Front Matter Richtig Nutzen"
teaser: "Jekyll Front Matter – Eigene Inhalte mit Metainformationen versorgen, erweitern sowie eigene Variablen für Templates und Themes definieren."
header:
    image: logo-jekyll.png
    background-color: "#333333"
image:
    thumb: icon/icon-jekyll.svg
chapter: "7"
permalink: /jekyll/front-matter/
breadcrumb: true
---
Der *front matter*-Bereich[^1] ist der Bereich eines Jekyll-Dokumentes, das Informationen über das Dokument enthält, also Metainformationen. So legen Sie über *front matter* z.B. Metainformationen wie Titel und welches Layout Jekyll für das aktuelle Dokument nutzen soll fest. Das sieht dann z.B. so aus:

~~~
---
layout: page
title:  "YAML front-matter richtig nutzen"
---
~~~

Wenn Jekyll ein Dokument liest, und Metainformationen innerhalb eines Bereiches findet, der oben und unten mit drei Minuszeichen startet und endet, prozessiert und speichert Jekyll diese Informationen ab und nutzt die Informationen, wenn diese abgefragt werden.

Damit *front matter* richtig funktioniert, muss das Dokument direkt mit den YAML-Informationen beginnen. Außerdem müssen die Informationen in der richtigen YAML-Syntax abgespeichert werden, damit Jekyll die Informationen lesen und verarbeiten kann.

> YAML ist eine vereinfachte Auszeichnungssprache zur Datenserialisierung, angelehnt an XML und an die Datenstrukturen in den Sprachen Perl, Python und C sowie dem in RFC 2822 vorgestellten E-Mail-Format. <cite>Quelle: [Wikipedia][2]</cite>

Dann entfaltet sich die Magie von Jekyll und die definierten Variablen (z.B. `title`) können über Liquid-Befehle genutzt und ausgegeben werden.



## Eigene Variablen über Front Matter definieren

Neben den von Jekyll vorgegebenen Standardwerten lassen sich auch eigene *front matter*-Variablen festlegen. Das ist die besondere Stärke von Jekyll. Denn neue Variablen legen Sie einfach im Front Matter fest. Wie Sie diese benennen, bleibt Ihnen überlassen. Wieviele Sie pro Dokument und Jekyll-Projekt definieren auch. Die Variablen können Sie wann immer Sie diese brauchen, in Templates, Schleifen und IF-Abfragen abrufen, ausgeben, kombinieren und nutzen.

Über die Konfigurationsdatei *_config.yml* können Sie für eigene Variablen auch [default-Werte festlegen][3]. Die Daten strukturieren Sie mit [YAML][1].



## Beispiel: YAML front-matter

~~~
---
layout: ""
title: ""
subtitle: ""
teaser: ""
image: ""
icon: ""
youtube-video-id: ""
embed: ""
comments: false
vgwortid: ""
categories: ""
date: 2014-06-19 00:00:00
tags: ["schlagwort-eins", "schlagwort-zwei"]
permalink: 
published: true
---
~~~



 [1]: http://yaml.org/
 [2]: http://de.wikipedia.org/wiki/YAML
 [3]: {{ site.url }}/jekyll/konfiguration/#voreinstellungen-fr-beitrge-festlegen
 [4]: #
 [5]: #
 [6]: #
 [7]: #
 [8]: #
 [9]: #
 [10]: #

 [^1]: Die offizielle Dokumentation finden Sie unter <http://jekyllrb.com/docs/frontmatter/>.
