---
layout: page-fullwidth
subheadline: Webdesign
title: "Responsive Webdesign mit dem Foundation Framework"
teaser: "Meine Responsive Websites baue ich mit Foundation. Foundation ist ein wunderbarer Werkzeugkasten, der aus HTML, CSS und Javascript-Funktionen besteht. Die Entwicklung von Responsive Webdesigns macht mit Foundation unglaublich Spaß und produziert professionelle Ergebnisse."
categories:
    - webdesign
tags:
    - css
    - foundation
    - framework
    - html
    - javascript
    - sass
    - webdesign
    - webentwicklung
    - artikel
image:
    thumb: icon/icon-foundation-128x.png
header:
    image_fullwidth: "webdesign-foundation-yeti.svg"
    background-color: "#335972"
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

## Warum ich Foundation nutze

[Foundation][1]&#8230;

* &#8230;wird konstant weiterentwickelt.
* &#8230;beschleunigt die professionelle Webentwicklung.
* &#8230;wurde in zahlreichen Browsern getestet.
* &#8230;hat eine exzellente [Dokumentation][2].
* &#8230;lässt sich leicht konfiguieren mit Hilfe von [Sass][3].
* &#8230;lässt sich leicht pflegen über das Terminal.
* {: .no-bullet }

## Foundation kurz ausprobieren

Für die ersten Schritte mit Foundation reicht der [Download oder der benutzerdefinierte Download des Frameworks][4].

## Foundation (richtig) installieren

Foundation macht erst richtig Spaß, wenn man das [Terminal][5] (Mac) nutzt, um anschließend die CSS-Datei mittels [Sass][3] zusammenschrauben zu lassen. Um Foundation zu installieren, tippt man die folgenden Befehle rein. Je nachdem, wie der eigene Rechner konfiguriert ist, muss man erst die Installation über das eigene Passwort erlauben. Dafür ist der Befehl `sudo` notwendig.

Da Foundation seit Version 5 die Kompenenten und Bestandteile des Frameworks mit Hilfe von Bower organisiert, muss man zuerst Bower installieren. Zuvor muss man die folgende Software auf seinem Rechner installieren. Das ist zu Anfang zwar ein wenig Arbeit, die sich später aber definitiv auszahlt.

*   Git
*   Ruby 1.9+
*   NodeJS

### Bower installieren

`sudo npm install -g bower grunt-cli`

### Foundation Gem installieren

`gem install foundation`

## Neues Foundation-Projekt anlegen

Um ein neues Projekt anzulegen, öffnet man einfach im Terminal das Verzeichnis, in welchem ein neues Projekt initiiert werden soll. Dann tippt man in die Kommandozeile folgenden Befehl, der das Projekt aufsetzt:

`foundation new NEUES_PROJEKT`

## Foundation-Projekte aktualisieren

Dank der neuen Methode per Bower, aktualisiert man Foundation-Projekte einfach und unkompliziert, indem man mit `cd` in das Projekt-Verzeichnis wechselt und mit dem Foundation-Befehl das Projekt aktualisiert:

`cd MEIN_Projekt`  
`foundation update`

## Loslegen mit Foundation

Wurde das Projekt angelegt, öffnet man einfach seinen Editor und öffnet im Verzeichnis die `index.html`-Seite. Diese hilft bei den ersten Schritten. Für weitere Informationen für Kompenenten, Attribute und Styles schaut Ihr in das [Foundation Manual][2].

 [1]: http://foundation.zurb.com
 [2]: http://foundation.zurb.com/docs/index.html
 [3]: http://mo.phlow.de/sass-compass/
 [4]: http://foundation.zurb.com/develop/download.html
 [5]: {{ site.url }}/terminal/


</div><!-- /.medium-7.columns -->
</div><!-- /.row -->
