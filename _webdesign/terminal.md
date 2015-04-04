---
layout: page
title:  "Terminal Befehle"
categories: development
---
**Table of Contents**
{: #toc }
*  TOC
{:toc}

## Gesamtes Verzeichnis samt Inhalt löschen

~~~
rm -rf verzeichnisname
~~~

## Versteckte Ordner und Dateien anzeigen

Damit der Finder alle versteckten Dateien und Ordner anzeigt, gibt man über das Terminal den folgenden Befehl ein.

~~~
defaults write com.apple.finder AppleShowAllFiles TRUE
~~~

Danach muss man den Finder neu starten, damit die Änderungen aktiv werden:

~~~
killall Finder
~~~

Um den Vorgang rückgängig zu machen, nutzt man den folgenden Befehl und startet erneut den Finder von vorne mit `killall Finder`.

~~~
defaults write com.apple.finder AppleShowAllFiles FALSE
~~~



## Verzeichnisinhalt in Datei speichern

Der Befehl `ls` gibt den Inhalt des aktuellen Ordners aus. Anstelle den Inhalt im Terminal auszugeben, kann man diesen umleiten. Mit `>` leitet man die Ausgabe in eine `.txt`-Datei um. Diese kann man dann in jedem Texteditor öffnen. 

~~~
$ ls > verzeichnisinhalt.txt
~~~

Die zusätzlichen Parameter `-la` sorgen dafür, dass die Dateien als ausführliche Liste mit allen Angaben ausgegeben werden.

~~~
$ ls -la > verzeichnisinhalt.txt
~~~

Über das Terminal kann man diese Datei auch unkompliziert mit `open verzeichnisinhalt.txt`. Noch schneller geht es, wenn man die Befehle miteinander verkettet.

~~~
$ ls > verzeichnisinhalt.txt;open verzeichnisinhalt.txt
~~~


## Bilder zuschneiden mit sips

### Bild anpassen und zurechtschneiden und Seitenverhältnis ignorieren

~~~
$ sips -z 768 1024 image.png
~~~

### Bild anpassen mit Seitenverhältnis

~~~
$ sips -Z 480 image.png
~~~


### Bilder passgenau zuschneiden und in angelegten Ordner thumbs speichern

~~~
sips -Z 150 -c 150 150 *.jpg --out thumbs
~~~


Mit --out bestimmt man entweder einen neuen Dateinamen oder einen Ordner, in welchen die bearbeiteten Dateien gespeichert werden.

Um eine Datei zu erstellen hängt man eine Dateiendung wie *.jpg* an:

~~~
sips -Z 150 -c 150 150 bild.jpg --out bild_thumb.jpg
~~~

Um die Dateien in einen Ordner namens thumb zu speichern, gibt man folgendes an:

~~~
sips -Z 150 -c 150 150 *.jpg --out thumbnails
~~~

<small>Quelle <http://www.apfelquak.de/2007/11/19/sips-bildbearbeitung-via-terminal/></small>


## WordPress runterladen, entpacken und Archiv löschen

~~~
$ wget http://wordpress.org/latest.tar.gz && tar xfz latest.tar.gz && rm -f latest.tar.gz
~~~


