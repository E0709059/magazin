---
layout: page
title:  "Ein neues Jekyll-Projekt erstellen"
teaser: "Mit einem kurzen Befehl starten Sie ein neues Jekyll-Projekt. Nachdem Jekyll die Website angelegt hat, starten Sie den integrierten Server mit einem zweiten Befehl und schon geht's los."
header:
    image: logo-jekyll.png
    background-color: "#333333"
image:
    thumb: icon/icon-jekyll.svg
chapter: "3"
permalink: /jekyll/projekt-erstellen/
breadcrumb: true
---

## Schritt 1: Neues Jekyll-Projekt initieren

Hat man Jekyll auf seinem Computer installiert, öffnet man als nächstes das Terminal. Um ein neues Jekyll-Projekt anzulegen, genügt der folgende Befehl:

{% include alert terminal='jekyll new jekyll-projekt' %}

Anschließend wechselt man mit...

{% include alert terminal='cd jekyll-projekt' %}

...in das Projektverzeichnis.



## Schritt 2: Jekyll-Server starten

Im zweiten Schritt genügt der kurze Befehl...

{% include alert terminal='jekyll serve' %}

..., um den in Jekyll eingebauten Server zu starten. Verändert man im Jekyll-Ordner Dateien, so erkennt Jekyll dies automatisch. Entdeckt das Programm Änderungen, baut es die Webseiten neu und speichert diese im Verzeichnis `_site` ab. In Kombination mit [Livereload][1] ist das eine unschlagbare Entwicklungsumgebung.



## Schritt 3: Jekyll-Website im Browser aufrufen

Über den Browser ruft man sein Jekyll-Projekt über `localhost:4000` auf.


## Jekyll stoppen mit CMD + C

Läuft Jekyll als Server oder baut Jekyll gerade eine Website mit dem Befehl...

{% include alert terminal='jekyll build' %}

..., dann lässt sich dieser Prozess mit <kbd>CMD</kbd> + <kbd>C</kbd> abbrechen.



 [1]: http://livereload.com/
 [2]: #
 [3]: #
 [4]: #
 [5]: #
 [6]: #
 [7]: #
 [8]: #
 [9]: #
 [10]: #