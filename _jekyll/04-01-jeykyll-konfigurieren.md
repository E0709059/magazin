---
layout: page
title:  "Die Jekyll-Website konfigurieren"
teaser: "Die Jekyll-Website konfiguiert man mit Hilfe der _config.yml-Datei. Und diese Optionen stehen zur Verfügung."
header:
    image: logo-jekyll.png
    background-color: "#333333"
image:
    thumb: icon/icon-jekyll.svg
chapter: "5"
permalink: /jekyll/konfiguration/
breadcrumb: true
---

Der nächste Schritt ist die Individualisierung der Jekyll-Website. Dazu öffnet man die Konfigurationsdatei `_config.yml`.

Um dem Projekt einen eigenen Namen zu geben, ändert man `name`. Da sämtliche Textdateien durch einen Markdown-Filter fließen, was einfach wunderbar ist, sollte man `markdown: redcarpet` erst einmal belassen. Wer weiss, dass er definitiv keine Code-Schnipsel auf seiner Jekyll-Site anzeigen lassen will, der stellt den Konverter *pygments* einfach aus. Das geschieht mit dem Wert `false`, als `pygments: false`.

Bei mir sieht das dann so aus:

{% highlight html %}
name: Webseiten bauen mit Jekyll
markdown: kramdown
highlighter: true
{% endhighlight %}


## Voreinstellungen für Beiträge festlegen

Über `defaults` lassen sich Voreinstellungen für Beiträge festlegen, damit man diese nicht immer und immer wieder für Beiträge neu eingeben muss.

Unten legt man für den `type` *posts* fest, dass diese standardmäßig als voreingestelltes Layout `default` bekommen und alle Dokumente einbezogen werden: `path: ""`. Im [YAML front-matter][2] kann man diese Einstellung natürlich pro Dokument überschreiben.

~~~
defaults:
  -
    scope:
      path: "" # ein leerer string an dieser Stelle bezieht alle Projektateien ein
      type: "posts"
    values:
      layout: "default"
~~~

<small>Quelle: <http://jekyllrb.com/docs/configuration/#front-matter-defaults></small>


## Weitere Konfigurationmöglichkeiten für Jekyll-Projekte


`port: 8888`
:	Um den Server-Port vom Standardwert `4000` z.B. auf `8888` umzustellen, nutzt man in der Konfiguration `port:`.

`encoding: UTF-8`
:	Um die Kodierung für Unicode-Zeichen auf [UTF-8][1] festzulegen – besonders hilfreich bei Jekyll-Projekten auf Windows – legt man diese mit `encoding: UTF-8` fest.





 [1]: http://de.wikipedia.org/wiki/Utf-8
 [2]: {{ site.url }}/anleitung/front-matter/
 [3]: #
 [4]: #
 [5]: #
 [6]: #
 [7]: #
 [8]: #
 [9]: #
 [10]: #