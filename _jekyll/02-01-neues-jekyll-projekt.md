---
layout: page
title:  "Ein neues Jekyll-Projekt erstellen"
teaser: "Ein Befehl reicht, um ein neues Jekyll-Profjekt zu initialisieren. Ein weiterer Befehl startet den integrierten Server."
header:
    image: logo-jekyll.png
    background-color: "#333333"
image:
    thumb: icon/icon-jekyll.svg
chapter: "3"
permalink: /jekyll/projekt-erstellen/
breadcrumb: true
---

## #1 Neues Jekyll-Projekt initieren

Hat man Jekyll auf seinem Computer installiert, reicht der einfache Befehl `jekyll new projektname` um eine neue Jekyll-Website zu erstellen.

<div class="alert-box radius terminal" markdown="1">
$ jekyll new jekyll-projekt  
</div>

Anschließend wechselt man mit...

<div class="alert-box radius terminal" markdown="1">
$ cd jekyll-projekt   
</div>

...in das Projektverzeichnis und startet von dort aus mit...

<div class="alert-box radius terminal" markdown="1">
$ jekyll serve  
</div>

...den eingebauten Jekyll-Server.



## #2 Jekyll-Server starten und Änderungen überwachen

Mit dem schnuckeligen Befehl `jekyll serve --watch` oder noch kürzer `jekyll serve -w` befiehlt man Jekyll einen Server zu starten und gleichzeitig den Ordner zu überwachen, in welchem man gerade arbeitet und Dokumente ändert. Entdeckt das Programm Änderungen, baut es die Website neu.

<div class="alert-box radius terminal" markdown="1">
$ jekyll serve -w
</div>


## #3 Jekyll-Website im Browser aufrufen

Über den Browser ruft man sein Jekyll-Projekt über `localhost:4000` auf.


## Jekyll stoppen mit CMD + C

Läuft Jekyll als Server oder baut gerade eine Website, dann lässt sich dieser Prozess mit <kbd>CMD</kbd> + <kbd>C</kbd> abbrechen.