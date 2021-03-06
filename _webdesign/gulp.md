---
layout: page
subheadline: "Webentwicklung"
title: 'Durchstarten mit Gulp.js – Websites optimieren, Arbeitsabläufe automatisieren'
teaser: "Mit Gulp.js automatisiert man Prozesse. Ob Minifizierung von Javascript, CSS und HTML, verlustlose Optimierung von Bildern oder z.B. die Kompilierung von Sass-Dateien: Gulp erledigt diese Prozesse in einem Rutsch, überwacht Veränderungen und revolutioniert die eigene Webentwicklung."
meta_description: "Mit Gulp.js automatisiert man Webdesign-Prozesse, wie die Minifizierung von Javascript, CSS und HTML oder optimiert verlustlos Bilder. Eine Anleitung."
categories:
  - webdesign
tags:
  - artikel
  - building tool
  - grunt
  - gulp
  - task runner
  - webdesign
  - webentwicklung
header:
  image: gulp-building-tool.png
  background-color: "#ffffff"
  caption: Gulp Beispiel Prozess
image:
  thumb: icon/icon-gulp-128x.png
permalink: /webdesign/gulp/
---
Obendrein operiert Gulp schneller als [Grunt][1] und ist leichter zu programmieren. Eine ausführliche Anleitung für den Taskrunner und das Building Tool Gulp.

<div class="panel radius" markdown="1">
Inhalt
{: #toc }
*  TOC
{:toc}
</div>


## Wie funktioniert das Building Tool Gulp.js? {#was-ist-gulp}

<img class="left" src="{{ site.urlimg }}gulp-2x.png" alt="gulp-2x" width="134" height="300">[Gulp.js][11] ist ein so genannter Task Runner basierend auf Node.js. Verglichen mit seinem Verwandten [Grunt][1], lässt sich Gulp verständlicher und schlanker programmieren. Vor allem liegt das am Konzept der Ströme, bzw. »Streams«.

Denn Aufgaben leitet man bei Gulp durch Kanäle, die »Pipes« – siehe Abbildung. Das hilft beim logischen Aufbau eines Arbeitsablaufes (Task) und beschleunigt den Prozess. Im Vergleich mit Grunt erledigt Gulp die gleiche Arbeit schneller, da nicht nach jedem Arbeitsprozess ein Schreibprozess notwendig ist. Dieser erfolgt erst bei Beendigung des Prozesses oder, wenn er ausdrücklich gewollt ist.

Außerdem arbeitet Gulp asynchron und arbeitet gleichzeit mehrere Aufgaben ab. Ein weiteres zugrundliegendes Konzept sind »einfache Plugins«. Gulp-Plugins werden für eine Aufgabe designt, nicht für mehrere. Grundlegende Funktionen, z.B. die Überwachung von Prozessen, sind in Gulp bereits implementiert.

> Unter asynchroner Kommunikation versteht man in der Informatik und Netzwerktechnik einen Modus der Kommunikation, bei dem das Senden und Empfangen von Daten zeitlich versetzt und ohne Blockieren des Prozesses durch bspw. Warten auf die Antwort des Empfängers (wie bei synchroner Kommunikation der Fall) stattfindet. <cite><a href="http://de.wikipedia.org/wiki/Asynchrone_Kommunikation">WikiPedia</a></cite> 


### Vorteile von Gulp.js in einer Nussschale

*   **Schneller** dank dem Konzept der asynchronen »Streams«
*   **Einfacher** zu programmieren
*   **Übersichtlichere** Konfigurationsdateien



## Tutorial–Zielsetzung: Was Gulp für uns erledigen soll

In diesem Tutorial soll Gulp in einem Rutsch für unsere mehrere Aufgaben abarbeiten. Dazu gehören die folgenden:

*   **Bilder** – Verlustlose Kompression aller Bilder und Vektoren mit `gulp-imagemin`
*   **HTML** – Minifizierung von mit `gulp-minify-html`
*   **Javascript** 
    *   Überprüfung mit `gulp-jshint`
    *   Zusammenfassen Javascripte mit `gulp-concat`
    *   Minifizierung Javascripts mit `gulp-uglify`
*   **CSS** 
    *   Konvertierung der Sass-Datei in eine CSS-Datei mit `gulp-sass`
    *   Autoprefixer, um alle Vendor Prefixes zu überprüfen mit `gulp-autoprefixer`
    *   Minifizierung der CSS-Datei mit `gulp-minify-css`
*   **Kopieren** aller Dateien in einen Ordner für den Upload
*   **Überwachung** von Dateien auf mögliche Änderungen

## Gulp installieren {#gulp-install}

Bevor man mit Gulp arbeiten kann, muss man zuerst Node.js installieren. Node.js kann man für Windows, Mac und Linux unter <nodejs.org/download/> herunterladen.

### #1 Node.js installieren

Node.js can be downloaded for Windows, Mac and Linux at nodejs.org/download/. You can also install it from the command line using a package manager.

Nach der Installation testet man sowohl Node.js als auch den dazugehörigen Paketmanager über das Terminal, um zu prüfen, ob die Installation erfolgreich war.

Mit&#8230;

{% include alert terminal='node -v' %}

&#8230;testet man, ob Node.js installiert ist und erhält die aktuelle Versionsnummer. Den Paketmanager überprüft man anschließend mit:

{% include alert terminal='npm -v' %}


    

### #2 Gulp installieren

Arbeiten beide Prozesse, installiert man Gulp mit dem folgenden Befehl:

{% include alert terminal='npm install gulp -g' %}

Der Parameter `-g` ist wichtig, um Gulp global auf dem System zu installieren. Auf Mac oder Linux-Rechnern kann es sein, dass man als Admin erst einmal ein Passwort für die Installation eingeben muss. Das erledigt man mit `sudo`. Wer sich nicht so gut mit dem Terminal auf dem Mac auskennt, der findet weitere hilfreiche Tipps in meinem [Terminal-Artikel][12]

{% include alert terminal='node -v' %}

Ob und welche Version von Gulp installiert ist, erfährt man über&#8230;

{% include alert terminal='gulp -v' %}


### #3 Initialzündung für das erste Projekt

Für diese Anleitung legen wir einen Ordner namens `foundation` an und springen in den Ordner. In diesem Ordner liegen sämtliche Dateien wie HTML, CSS, Javascripte, Bilder und Sass-Dateien des Beispielprojektes. Damit man Gulp nutzen kann, muss man es im nächsten Schritt lokal installieren.

Zuvor legen wir noch eine `package.json`-Datei an. In dieser notiert der Packetmanager automatisch, welche Version der Module und welche Module installiert wurden. Die `package.json`-Datei ist nicht für den Betrieb notwendig, ist aber schnell über `npm init` oder `echo '{}' > package.json` angelegt. Anschließend installiert man Gulp. Und so sehen die Befehle dann aus:

{% include alert terminal='npm init' %}

{% include alert terminal='npm install gulp --save-dev' %}

Jetzt muss man nur noch die Steuerungsdatei `gulpfile.js` für Gulp anlegen. In diese Datei tippt man sämtliche Aufgaben, die das Building Tool für uns erledigen soll.

## Gulp Plugins installieren {#gulp-install}

Plugins installiert man über den Befehl `npm install plugin-name --save-dev`. Der Parameter `--save-dev` befiehlt dem Paketmanager das Paket herunterzuladen und in `package.json` zu notieren.

Für dieses Tutorial installieren wir die folgenden Plugins.

{% include alert terminal='npm install gulp-imagemin --save-dev' %}
{% include alert terminal='npm install gulp-changed --save-dev' %}
{% include alert terminal='npm install gulp-minify-html --save-dev' %}
{% include alert terminal='npm install gulp-jshint --save-dev' %}
{% include alert terminal='npm install gulp-concat' %}
{% include alert terminal='npm install gulp-uglify --save-dev ' %}
{% include alert terminal='npm install gulp-sass' %}
{% include alert terminal='npm install gulp-autoprefixer --save-dev ' %}
{% include alert terminal='npm install gulp-minify-css --save-dev ' %}

Anstelle jeden Befehl einzeln einzugeben, kann man sämtliche Plugins auch über einen Befehl installieren. Dazu reiht man die Namen einfach aneinander. Der folgende Befehl installiert drei Plugins nacheinander in einem Rutsch und notiert sie in `package.json`.

{% include alert terminal='npm install gulp-imagemin gulp-uglify gulp-minify-css --save-dev' %}



## Gulp samt Plugins in gulpfile.js einbauen {#gulpfile}

Hat man die Plugins installiert – man kann weitere später nachrüsten –, öffnet man als nächstes `gulpfile.js`. Dort registriert man jetzt sämtliche benötigten Plugins und zuallererst natürlich Glulp selbst. Das geschieht mit&#8230;

{% highlight javascript %}
// gulp.js einbauen
var gulp = require('gulp'); 
{% endhighlight %}

Im nächsten Schritt baut man die Plugins ein. Um nicht jede Zeile mit `var` zu beginnen, kann man auch alle Plugins über ein Komma nacheinander definieren. Nur zum Schluss darf man das Semikolon nicht vergessen.

{% highlight javascript %}
// Plugins einbauen
var changed = require('gulp-changed'),
    jshint = require ('gulp-jshint'),
    concat = require ('gulp-concat'),
    uglify = require ('gulp-uglify'),
    rename = require('gulp-rename'),
    imagemin = require ('gulp-imagemin'),
    clean = require('gulp-clean'),
    minifyhtml = require ('gulp-minify-html'),
    autoprefixer = require ('gulp-autoprefixer'),
    minifyCSS = require ('gulp-minify-css');
{% endhighlight %}



## Komprimieren von Bildern und Vektorgrafiken – PNG, SVG, JPG, GIF {#images}

Zur einfachsten und oft auch wirkungsvollsten Methode die eigene Website zu beschleunigen, gehört die Optimierung von Bildern. Diese Aufgabe übernimmt das Plugin *imagemin*. Damit die Bilder nicht immer und immer wieder erneut optimiert werden, nutzen wir ein weiteres Plugin, dass die bereits getätigten Änderungen überwacht: `gulp-changed`.

Und so sieht dann der Task aus:

{% highlight javascript %}
// Komprimiere Bilder
gulp.task('images', function() {
  var imgSrc = './src/images/**/*',
      imgDst = './build/images';

  gulp.src(imgSrc)
    .pipe(changed(imgDst))
    .pipe(imagemin())
    .pipe(gulp.dest(imgDst));
});
{% endhighlight %}

In der ersten Zeile definiert man die Aufgabe und benennt sie, hier `images`. Die darauffolgenden Zeilen definieren zwei Variablen, mit denen man das Quellverzeichnis `imgSrc` der noch nicht optimierten Bilder definiert und das Zielverzeichnis `imgDst`, in welches Gulp die optimierten Bilder speichern soll.

Mit `gulp.src(imgSrc)` startet man den Task und übergibt das in Variable `imgSrc` festgelegte Verzeichnis. Anschließend befiehlt man mit `changed` nur neue Dateien zu komprimieren, das spart Zeit. Im nächsten Schritt schleust man endlich die Bilder mit `.pipe(imagemin())` durch das Plugin. Ganz wichtig ist der letzte Befehl `.pipe(gulp.dest(imgDst))`. Ohne `gulp.dest` werden die Bilder zwar optimiert, aber nicht abgespeichert. Denn das erledigt Gulp erst mit der letzten Zeile.

Jetzt speichert man `gulpfile.js` ab und startet die Aufgabe über die Konsole mit `gulp` + `Name der Aufgabe`, also:

{% include alert terminal='gulp images' %}

Jetzt sollte Gulp nach Bildern im Quellverzeichnis `./src/images/**/*` suchen, bearbeiten und im Zielverzeichnis `./build/images` speichern. Damit auch alle Bilddateien erwischt werden, befehlen wir Gulp mit dem Sternchen `*` sämtliche Dateien zu bearbeiten. Mit `*.jpg` würden wir z.B. nur die JPG-Dateien aussuchen.

Damit Gulp auch Bilder in Unterverzeichnissen von `src/images/` berüchsichtigt, kommt noch ein Parameter dazu, die zwei Sternchen `**`. Damit krabbelt Gulp auch durch alle Unterverzeichnisse.

Mehr zu den beiden benutzten Plugins findet man unter:

gulp-imagemin
:   <https://www.npmjs.org/package/gulp-imagemin>
:   <https://github.com/sindresorhus/gulp-imagemin>

gulp-changed
:   <https://www.npmjs.org/package/gulp-changed>
:   <https://github.com/sindresorhus/gulp-changed>


## Grundlegende Links {#gulp-links}

*   [Gulp Website][11]
*   [gulp API docs][13]
*   [Gulp Cheatsheet][14]



## Hilfreiche Gulp-Plugins

### Gulp FTP

Mit *gulp-ftp* lädt man Dateien hoch. Kombiniert man *gulp-ftp* mit der *watch*-Funktion so befiehlt man Gulp die Überwachung von Dateien und Ordnern und initiert bei einer neuen Datei einen automatischen Upload. Dahingegen lassen sich mit dem Plugin jedoch keine Dateien können per FTP löschen. löschen. Eine Alternative ist evtl. *rsync*. Mehr dazu im Artikel [»Deploying via rsync with Gulp«][15]

<https://github.com/sindresorhus/gulp-ftp>



## Gulp Tutorials (Text) {#tuts-text}


### Deutsche Tutorials

*   [Front-end Workflow mit Gulp][16]


### Englische Tutorials

* Mark Goodyear: [»Getting started with gulp«][17]
* Sitepoint: [»An Introduction to Gulp.js«][18]
* Smashing Magazine: [»Building With Gulp«][19]
* Julien Renaux: [»Introduction to Gulp.js with practical examples«][20]
* Justin McCandless: [»A Tutorial for Getting Started with Gulp«][21]
* [9 gulp.js plugins for a great build system][22]
* [Deploying via rsync with Gulp][15]



## Gulp Video Tutorials {#tuts-video}

### LevelUpTuts – Learning Gulp

Die LevelUpTuts-Videoanleitungen holen auch Anfänger mit grundlegenden Webdesign-Kenntnissen ab. Diese Tutorial-Serie war für mich die Initialzündung, um mich mit Gulp auseinanderzusetzen.

<div class="flex-video"><iframe width="1280" height="720" src="//www.youtube.com/embed/videoseries?list=PLLnpHn493BHE2RsdyUNpbiVn-cfuV7Fos" frameborder="0" allowfullscreen></iframe></div><!-- /.flex-video -->



### Gulp Tutorials von Maximilian Schmitt

Diese Serie ist für Fortgeschrittene und Kenner von Javascript und Node.js geeignet.

* [Get started with gulp Part 1: Workflow overview and jade templates][23]
* [Get started with gulp Part 2: gulp & Browserify][24]
* [Get started with gulp Part 3: Uglify & environment variables][25]
* [Get started with gulp Part 4: SASS & CSS minification][26]
* [Get started with gulp Part 5: gulp.watch for true automation][27]
* [Get started with gulp Part 6: LiveReload and web server  
    ][28]



## Grunt.js vs. Gulp.js &#8211; Interview mit Stefan Baumgartner {#gulp-grunt}

<div class="flex-video"><iframe width="1280" height="720" src="https://www.youtube.com/embed/NyQHh3HkcZE" frameborder="0" allowfullscreen></iframe></div><!-- /.flex-video -->


 [1]: http://mo.phlow.de/grunt/
 [11]: http://gulpjs.com/
 [12]: http://mo.phlow.de/terminal/
 [13]: https://github.com/gulpjs/gulp/blob/master/docs/API.md
 [14]: https://github.com/osscafe/gulp-cheatsheet
 [15]: http://www.evendev.com/blog/rsync-deploys-with-gulp.html
 [16]: http://liechtenecker.at/front-end-workflow-mit-gulp/
 [17]: http://markgoodyear.com/2014/01/getting-started-with-gulp/
 [18]: http://www.sitepoint.com/introduction-gulp-js/
 [19]: http://www.smashingmagazine.com/2014/06/11/building-with-gulp/
 [20]: http://julienrenaux.fr/2014/05/25/introduction-to-gulp-js-with-practical-examples/
 [21]: http://www.justinmccandless.com/blog/A+Tutorial+for+Getting+Started+with+Gulp
 [22]: http://blog.nodejitsu.com/npmawesome-9-gulp-plugins/
 [23]: https://www.youtube.com/watch?v=DkRoa2LooNM
 [24]: https://www.youtube.com/watch?v=78_iyqT-qT8
 [25]: https://www.youtube.com/watch?v=gRzCAyNrPV8
 [26]: https://www.youtube.com/watch?v=O_0S6Z9FIKM
 [27]: https://www.youtube.com/watch?v=nsMsFyLGjSA
 [28]: https://www.youtube.com/watch?v=KURMrW-HsY4