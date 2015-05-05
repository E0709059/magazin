---
layout: page
subheadline: "Static Website Generator"
title: "Was ist Jekyll?"
meta_title: "Was ist Jekyll? Und was ist ein Static Website Generator?"
teaser: "Einführung in Jekyll. Dieser Artikel erklärt die Funktionsweise sowie die Pro und Cons des kostenlosen Website Generators von GitHub."
image:
    thumb: icon/icon-jekyll.svg
chapter: "1"
permalink: /jekyll/was-ist-jekyll/
---
[Jekyll][1] ist ein so genannter *Static Website Generator*. Das Kommandozeilenprogramm bietet keine [WYSIWYG][2]-Oberfläche, sondern man startet es über die Kommandozeile – z.B. über das Terminal bei Mac.

Jekyll generiert bzw. baut statische HTML-Webseiten. Das in Ruby geschriebene Programm eignet sich hervorragend für den Betrieb eines Blog oder für kleine Website-Projekte, wie z.B. Portfolios, Minisites oder kleine Image-Websites.

> Website generators like Jekyll work by combining template files with content and rendering them to static html pages. They provide the best balance between content creation and editing flexibility, serving an incredibly fast and reliable website.

Die Stärken liegen auf der Hand: Da Jekyll nur statische Webseiten generiert, entstehen keine Sicherheitslücken auf dem Server. Außerdem man muss kein Redaktionssystem samt Plugins pflegen, denn Jekyll baut die Website auf dem eigenen Rechner, die man  anschließend per FTP-Programm nur noch hochladen muss. So entfallen Wartungsarbeiten, wie sie z.B. beim [CMS WordPress][3] kontinuierlich anfallen.

> I was originally going to name it Conveyor (because the project was to take one type of file and conveyor belt it through a process that turned it into another format), but I think that was already taken as a gem name. So I thought about it and decided that the most important feature was the ability to transform files of a rather bland format into files that were so much more interesting. This transformation process reminded me of the story of Dr Jekyll and Mr Hyde, and the name jekyll was available as a gem and seemed to encapsulate the ideas of transformation that I wanted. Thus: Jekyll was born!


## Die Stärken eines Static Website Generators

Jekyll bietet als Static Website Generator zahlreiche Vorteile, die Systeme wie WordPress einfach nicht bieten können. Die wichtigsten Vorteile von Jekyll sind:

* Kaum Serverlast durch statische HTML-Seiten
* Schnelle Performance der Website für gute Suchmaschinenpositionen
* Sicherheit der Webpräsenz dank reinem HTML
* Texte schreibt man im eigenen Lieblingseditor
* Sehr flexible Gestaltung von Templates
* Einfache Entwicklung und Pflege
* Versionskontrolle durch kontinuierliche Backups
* Unkomplizierter Umzug von Websites
* Software- und Formatunabhängigkeit


## Wie funktioniert Jekyll?

Jeykyll arbeitet als Kommandozeilenprogramm und generiert Webseiten anhand von Textdokumenten und Templates. Eine Datenbank benötigt Jekyll nicht, da beim Start von Jekyll sämtliche Projektdateien indiziert werden und die Metainformationen temporär gespeichert werden.

<div class="alert-box info radius" markdown="1">
TIPP: **Ich möchte von WordPress zu Jekyll wechseln, was nun?**

Das beste Werkzeug um alte WordPress-Beiträge in das Jekyll-Format zu konvertieren ist [Exit WP][4]. Die Beiträge konvertiert das Werkzeuge anhand der wordpress.xml-Datei, die man über das WordPress-Backend unter Werkzeuge exportiert.
</div>






 [1]: http://jekyllrb.com/
 [2]: http://de.wikipedia.org/wiki/WYSIWYG
 [3]: http://phlow.de/wordpress
 [4]: https://github.com/thomasf/exitwp
 [5]: #
 [6]: #
 [7]: #
 [8]: #
 [9]: #
 [10]: #