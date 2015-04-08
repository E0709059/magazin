---
layout: page-fullwidth
title: "Grundlegende Terminal Befehle"
teaser: "Webdesigner, die sich mit dem Terminal beschäftigen – <em>insbesondere auf Mac-Rechnern</em> – werden schnell feststellen, wie flexibel, schnell und komfortabel die Arbeit mit der Kommandozeile sein kann. Und wenn Sie einen Befehl vergessen haben, müssen Sie nur wissen, wo Sie nachschauen müssen. Genau hier :)"
categories:
    - development
tags:
    - artikel
image:
    thumb: icon/icon-terminal-128x.png
header:
    image: icon/terminal-256x.png
    background-color: "#f5b6c9"
style: "#masthead-with-background-color { padding: 0; }"
---
<div class="row">
<div class="medium-5 medium-push-7 columns" markdown="1">
<div class="panel radius" markdown="1">
**Inhalt**
{: #toc }
*  TOC
{:toc}
</div>
</div><!-- /.medium-5.columns -->



<div class="medium-7 medium-pull-5 columns" markdown="1">

## Verzeichnis mit Inhalt löschen

{% include alert terminal='rm -rf verzeichnisname' %}




## Versteckte Ordner & Dateien anzeigen

Damit Finder alle versteckten Dateien und Ordner anzeigt, gibt man über das Terminal den folgenden Befehl ein.

{% include alert terminal='defaults write com.apple.finder AppleShowAllFiles TRUE' %}




Danach muss man den Finder neu starten, damit die Änderungen aktiv werden:

{% include alert terminal='killall Finder' %}

Um den Vorgang rückgängig zu machen, nutzt man den folgenden Befehl und startet erneut den Finder von vorne mit `killall Finder`.

{% include alert terminal='defaults write com.apple.finder AppleShowAllFiles FALSE' %}



## Verzeichnis als Textdatei speichern

Der Befehl `ls` gibt den Inhalt des aktuellen Ordners aus. Anstelle den Inhalt im Terminal auszugeben, kann man diesen umleiten. Mit `>` leitet man die Ausgabe in eine `.txt`-Datei um. Diese kann man dann in jedem Texteditor öffnen. 

{% include alert terminal='ls > verzeichnisinhalt.txt' %}


Die zusätzlichen Parameter `-la` sorgen dafür, dass die Dateien als ausführliche Liste mit allen Angaben ausgegeben werden.

{% include alert terminal='ls -la > verzeichnisinhalt.txt' %}


Über das Terminal kann man diese Datei auch unkompliziert mit `open verzeichnisinhalt.txt`. Noch schneller geht es, wenn man die Befehle miteinander verkettet.

{% include alert terminal='ls > verzeichnisinhalt.txt;open verzeichnisinhalt.txt' %}





## Bilder zuschneiden mit sips

### Bild anpassen und zurechtschneiden und Seitenverhältnis ignorieren

{% include alert terminal='sips -z 768 1024 image.png' %}




### Bild anpassen mit Seitenverhältnis

{% include alert terminal='sips -Z 480 image.png' %}





### Bilder passgenau zuschneiden und in angelegten Ordner thumbs speichern

{% include alert terminal='sips -Z 150 -c 150 150 *.jpg --out thumbs' %}





Mit --out bestimmt man entweder einen neuen Dateinamen oder einen Ordner, in welchen die bearbeiteten Dateien gespeichert werden.

Um eine Datei zu erstellen hängt man eine Dateiendung wie *.jpg* an:

{% include alert terminal='sips -Z 150 -c 150 150 bild.jpg --out bild_thumb.jpg' %}




Um die Dateien in einen Ordner namens thumb zu speichern, gibt man folgendes an:

{% include alert terminal='sips -Z 150 -c 150 150 *.jpg --out thumbnails' %}




<small>Quelle <http://www.apfelquak.de/2007/11/19/sips-bildbearbeitung-via-terminal/></small>


## WordPress runterladen, entpacken und Archiv löschen

{% include alert terminal='wget http://wordpress.org/latest.tar.gz && tar xfz latest.tar.gz && rm -f latest.tar.gz' %}





</div><!-- /.medium-7.columns -->
</div><!-- /.row -->
