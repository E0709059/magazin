---
layout: default
icon: webdesign.png
title: "Webdesign Workflow"
menutitle: "Webdesign Workflow"
description: "Workflow für den Website-Bau"
tags:
	- webdesign
	- workflow
---

> »**Lastly, it's the right thing to do.** It's almost impossible to do anything these days without directly or indirectly executing huge amounts of open source code. If you use the internet, you're using open source. That code represents millions of man-hours of time that has been spent and then given away so that everyone may benefit. We all enjoy the benefits of open source software, and I believe we are all morally obligated to give back to that community. If software is an ocean, then open source is the rising tide that raises all ships.« <cite>[Tom Preston-Werner][19] (GitHub Gründer/CEO) in »Open Source (Almost) Everything«</cite>



## Stift & Papier: Analoge Planung

Jede Website beginnt mit einer Idee, einem Sketch und einem Plan. Am Besten eignet sich dafür immer noch das alte gute Duo Stift & Papier.




## Foundation: Responsive Webdesign Templates 

<img class="left-align" src="<%= @getThumbnail("images/foundation.png", '128x128') %>" alt="">[Foundation][1] gehört zu den vielseitigsten CSS-Frameworks, um Responsive Webdesigns zu realisieren. So umfasst es ein Spaltenraster (Grid), mit dem sich einfach die verschiendesten Layouts für PCs und Mobilgeräte entwerfen lassen. Gemeinsam mit [jQuery][13] steuert man CSS-Klassen für etliche Bedienelemente wie etwa Navigation, Buttons, Dropdowns, Tabs, Slider, Accordion, Tooltips oder Pop-Ups. Foundation funktioniert mit alten Browsern bis zurück zum Internet Explorer 8.

### Lizenzen

   - Foundation: [MIT License][6]
   - jQuery: [MIT License][6]

### Praxis: Aufbau der Website

1. Layout
	1. Startseite
	2. Blog-Indexseite
	3. Blog-Beitrag
	4. About-Webseite
	5. Info-Webseite
	6. Video-Webseite
3. Navigation
4. Slider
5. Footer




## Sass & Compass: Layout, Typografie und weitere CSS-Elemente

<img class="left-align" src="<%= @getThumbnail("images/sass.png", '128x128') %>" alt="">[Sass][3] ist eine CSS-Metasprache. Mit Hilfe der SassScript-Syntax erweitert man CSS um Variablen, wiederverwendbare Code-Schnipsel und Funktionen, die CSS-Eigenschaften berechnen können.

<img class="right-align" src="<%= @getThumbnail("images/compass.png", '128x128') %>" alt="">[Compass][2] bezeichnet sich selbst als *CSS Authoring Framework*. Dabei handelt es sich bei Compass um einen Pre-Prozessor. Dieser Pre-Prozessor verwandelt SassScripte in einwandfrei funktionierende CSS-Dateien. Auf Wunsch kombiniert Compass mehrere Sass-Dateien zu einer CSS-Datei und komprimiert/minifiziert diese.

Um Compass zu nutzen, benötigt man einen Ruby-Interpreter auf seinem Rechner und das RubyGem Compass. Ruby ist eine Programmiersprache. Als RubyGem – oder kurz nur Gem – bezeichnet man ein Code-Paket mit welchem man Ruby erweitert (hier z.B. das Code-Paket für Compass). Übersetzt bedeutet Gem »Edelstein«, »Kostbarkeit« oder »Ding«.

### Lizenzen

   - Sass: [MIT License][6]
   - Ruby: [Ruby’s License][8]
   - Compass ist [Charityware][9]

### Praxis: Styling der CSS-Elemente

1. Farben
2. Typografie
	1. Überschriften mit [Pacifico][14]  
	2. Fließtext mit [Open Sans][15]
	3. Icons mit [Entypo][11]
	4. Code einfügen  
	`<link href='http://fonts.googleapis.com/css?family=Open+Sans:400italic,700italic,400,700|Pacifico' rel='stylesheet' type='text/css'>`
3. Header
4. Footer





## Node.js: Arbeitsplattform für Webdesigner

<img class="left-align" src="<%= @getThumbnail("images/nodejs.png", '128x128') %>" alt="">»[Node.js][4] ist eine serverseitige Plattform zum Betrieb von Netzwerkanwendungen. So realisiert man mit Node.js z.B. Webserver. Node.js basiert auf der JavaScript-Laufzeitumgebung ›V8‹, die ursprünglich für den Chrome-Browser entwickelt wurde und bietet eine ressourcensparende Architektur, die eine besonders große Anzahl gleichzeitig bestehender Netzwerkverbindungen ermöglicht.« <cite>[Wikipedia][12]</cite>

Lizenz: [MIT License][6]




## DocPad: Baumaschine und CMS für die Website

<img class="left-align" src="<%= @getThumbnail("images/docpad.png", '128x128') %>" alt="">DocPad ist eine Webseiten-Baumaschine. Die Anwendung basiert auf Node.js und Express.js. Über das Dateisystem lässt sich DocPad als Redaktionssystem (CMS) nutzen und generiert (rendert) über Plugins statische HTML-Webseiten.

DocPad ist eine Art Schweizer Taschenmesser für Webdesigner, denn mit DocPad kann man nicht nur Webseiten bauen, sondern auch eBooks, HTML-Präsentationen und ähnliches.

Lizenz: [MIT License][6]

### Praxis: Das Template zum Leben erwecken

1. DocPad-Website initialisieren
1. Plugins installieren
	1. Eco – 
	2. Marked – Konverter für [Markdown][17]-Texte
	3. Partials
	4. Thumbnail – benötigt [ImageMagick][18]
	5. Sitemap
	6. Related
1. DocPad-Website konfigurieren
1. Templates in Partials zerlegen
1. Beiträge anlegen





## Grunt: Optimierung und Minifizierung der Website

<img class="left-align" src="<%= @getThumbnail("images/grunt.png", '128x128') %>" alt="">Mit [Grunt][7] automatisiert man sich wiederholende Aufgaben bei der Webentwicklung. Grunt ist ein JavaScript-basierter Taskrunner und hilft unter anderem bei der Code-Minifizierung, Code-Kontrolle, Kompilierung, Unit Testing und so weiter. 

Lizenz: [MIT License][6]




[1]: http://foundation.zurb.com/
[2]: http://compass-style.org/
[3]: http://sass-lang.com/
[4]: http://nodejs.org/
[5]: http://docpad.org/
[6]: http://opensource.org/licenses/MIT
[7]: http://gruntjs.com/
[8]: https://www.ruby-lang.org/en/about/license.txt
[9]: https://www.kintera.org/AutoGen/Simple/Donor.asp?ievent=420320&en=htKJIXOKJlLQJXOMIgLJLXMKLeKVLcOKIbIOL3NGIjI5KmK
[10]: #
[11]: http://www.entypo.com/
[12]: http://de.wikipedia.org/wiki/NodeJS
[13]: http://jquery.com/
[14]: http://www.google.com/fonts/specimen/Pacifico
[15]: http://www.google.com/fonts/specimen/Open+Sans
[17]: http://daringfireball.net/projects/markdown/
[18]: http://www.imagemagick.org/script/index.php
[19]: http://tom.preston-werner.com/2011/11/22/open-source-everything.html
[20]: #
[21]: #
[22]: #
[23]: #
[24]: #
[25]: #
[27]: #
[28]: #
[29]: #






<small>Icon:  [»Flat design vector illustration of mobile and desktop website« von Shutterstock](http://www.shutterstock.com/pic.mhtml?id=151359191&src=id)</small>