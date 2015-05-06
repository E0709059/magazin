---
layout: page
title:  "YAML front-matter richtig nutzen"
teaser: "Jekyll front-matter – Eigene Inhalte mit Metainformationen versorgen, erweitern sowie eigene Variablen für Templates und Themes definieren."
header:
    image: logo-jekyll.png
    background-color: "#333333"
image:
    thumb: icon/icon-jekyll.svg
chapter: "7"
permalink: /jekyll/front-matter/
breadcrumb: true
---
Der *front-matter*-Bereich ist der Bereich eines Jekyll-Dokumentes, der Informationen zum Dokument enthält, also Metainformationen. So legt man über diese Metainformationen z.B. fest, welchen Titel und welches Layout Jekyll für das aktuelle Dokument nutzen soll. Das sieht dann z.B. so aus:

~~~
---
layout: page
title:  "YAML front-matter richtig nutzen"
---
~~~

Wenn Jekyll ein Dokument also liest, und Metainformationen innerhalb eines Bereiches findet, der oben und unten mit drei Minuszeichen startet und endet, prozessiert und speicher Jekyll diese Informationen ab und nutzt die Informationen, wenn diese an anderer Stelle abgefragt werden.

Damit front-matter richtig funktioniert, muss das Dokument direkt mit den YAML-Informationen beginnen. Außerdem müssen die Informationen in der richtigen YAML-Syntax abgespeichert werden, damit Jekyll die Informationen lesen und verarbeiten kann. Denn dann wird es richtig magisch und die definierten Variablen (z.B. `title`) können dann über Liquid-Befehle genutzt und ausgegeben werden.

> YAML ist eine vereinfachte Auszeichnungssprache zur Datenserialisierung, angelehnt an XML und an die Datenstrukturen in den Sprachen Perl, Python und C sowie dem in RFC 2822 vorgestellten E-Mail-Format. <cite>Quelle: [Wikipedia][2]</cite>

Neben den von Jekyll vorgegebenen Standardwerten lassen sich auch eigene front-matter-Variablen  festlegen. Das ist die Besondere Stärke von Jekyll, denn neue Variablen legt man einfach und nutzt Sie in Templates und Jekyll-Dokumenten.

Über die Konfigurationsdatei `_config.yml` [default-Werte  festlegen][3]. Die Daten strukturiert man mit  [YAML][1].






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

Offizielle Dokumentation: <http://jekyllrb.com/docs/frontmatter/>


 [1]: http://yaml.org/
 [2]: http://de.wikipedia.org/wiki/YAML
 [3]: http://jekyllrb.com/docs/configuration/#frontmatter-defaults
 [4]: #
 [5]: #
 [6]: #
 [7]: #
 [8]: #
 [9]: #
 [10]: #