---
layout: page-fullwidth
title: "Grundlegende Terminal Befehle"
teaser: "Mit Hilfe des Mac Terminals arbeiten Sie oft schneller, automatisieren nervige Prozesse und erledigen lästige Arbeit mit ein paar wenigen eingetippten Befehlen anstelle von Klickorgien. Vor allem als  Webdesigner werden Sie schnell feststellen, wie flexibel, schnell und komfortabel die Arbeit mit der Kommandozeile sein kann."
categories:
    - development
tags:
    - artikel
    - terminal
    - produktivität
image:
    thumb: icon/icon-terminal-128x.png
header:
    image: icon/terminal-256x.png
    background-color: "#f5b6c9"
style: "#masthead-with-background-color { padding: 0; }"
permalink: /terminal/
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


## Die wichtigsten Terminal Befehle

Der schnellste Weg das Terminal zu starten ist [Spotlight][1]. Einfach die Tastenkombination <kbd>CMD + Space</kbd> plus die Anfangsbuchstaben <kbd>ter</kbd> eingeben und <kbd>Enter</kbd> drücken. 

### Wichtige Begrifflichkeiten zuerst

directory
:    Verzeichnisse werden *directory* genannt.

home directory
:    Als *home directory* wird das Arbeitsverzeichnis, in welchem das Terminal startet – in der Regel `/Users/Name/`.


## Schneller mit dem Terminal arbeiten

### Pfeiltasten rauf und runter

Die Rauf- und Runterpfeiltasten wechseln zwischen den zuletzt eingetippten Befehlen

### Autovervollständigen mit der Tabulatortaste

Um schneller in Verzeichnisse zu springen, tippt man <kbd>cd</kbd> und dann die Anfangsbuchstaben des Verzeichnisses und mittendrin die Tabulatortaste. Das Terminal vervollständigt automatisch die Eingabe, sofern nicht mehrere Verzeichnisse mit der gleichen Zeichenfolge existieren.

### Wiederkehrende Befehlsketten als Stapelverarbeitung speichern

Will man eine Kette von Befehlen nacheinander vom Terminal abarbeiten lassen, legt man dazu am Besten eine so genannte *Batch-Datei* an. Hierbei handelt es sich um eine einfache Textdatei **ohne Dateiendung**.

In jede Zeile kopiert man einen Befehl, der abgearbeitet werden soll. Damit diese Datei ausgeführt werden kann, müssen die Rechte geändert werden.

Lautet die Batch-Datei z.B. *stapelverarbeitung* muss man die Rechte mit Hilfe des *chmod*-Befehls auf 755 stelle.

Der Befehl wäre dann <kbd>chmod 755 stapelverarbeitung</kbd>. Soll die Batch-Datei ausgeführt werden, springt man in das Verzeichnis, in welcher die Datei liegt und tippt vor dem Batch-Dateinamen noch <kbd>./</kbd> ein. In diesem Beispiel <kbd>./stapelverarbeitung</kbd>. Ohne <kbd>./</kbd> würde das Terminal den Befehl *stapelverarbeitung* suchen.



## Terminal individualisieren und verbessern

### Farbschemata ändern

Die Farbschemata für das Terminal ändert man über <kbd>CMD + ,</kbd> bzw. über das Menü *Terminal › Einstellungen › Einstellungen*. Um ein neues Farbschemata samt Typografieeinstellungen als Standard festzulegen, klickt man unten links auf *Standard*. Spannende Farbschemata sind z.B. diese hier:

* [Solarized](http://ethanschoonover.com/solarized)
* [Tomorrow Night (Terminal Version)](https://github.com/chriskempson/tomorrow-theme/blob/master/OS%20X%20Terminal/Tomorrow%20Night.terminal)

Um die obigen Farbschemata abzuspeichern, geht man wie folgt vor:

1. Datei herunterladen, die auf `.terminal` endet.
2. In einem Ordner abspeichern (wo man es bei Bedarf wiederfindet) und dann Doppelklicken.
3. Eventuell muss man die Sicherheitseinstellungen des Rechners kurz für die Installation außer Kraft setzen.
4. Nachdem sich das Terminal-Fenster mit dem neuen Farbschemata geöffnet hat, öffnet man die Einstellungen (siehe oben).
5. Ein Klick auf *Standard* macht es zum neuen Standardfarbschemata.






## Verzeichnis mit Inhalt löschen

{% include alert terminal='rm -rf verzeichnisname' %}



## Versteckte Ordner & Dateien mit Terminal anzeigen

Mit <kbd>ls</kbd> listet man die Dateien in einem Ordner auf. Um auch versteckte Dateien anzeigen zu lassen, muss man den Parameter <kbd>-all</kbd> oder in der Kurzvariante <kbd>-a</kbd> hinzufügen. Der Befehl lautet dann:

{% include alert terminal='ls -a' %}




## Versteckte Ordner & Dateien mit Finder anzeigen

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

Mit `--out` bestimmt man entweder einen neuen Dateinamen oder einen Ordner, in welchen die bearbeiteten Dateien gespeichert werden.

Um die Dateien in einen Ordner namens *thumbnails* zu speichern, gibt man folgendes an:

{% include alert terminal='sips -Z 150 -c 150 150 *.jpg --out thumbnails' %}

Wenn Sie nur eine Datei mit einer neuen Dateiendung zu erstellen – z.B. *.jpg* – dann hängen Sie die Endung einfach so an:

{% include alert terminal='sips -Z 150 -c 150 150 bild.jpg --out bild_thumb.jpg' %}







<small>Quelle <http://www.apfelquak.de/2007/11/19/sips-bildbearbeitung-via-terminal/></small>


### Dateiformat der Bilder konvertieren

{% include alert terminal='for i in *.png; do sips -s format jpeg $i --out konvertiert/$i.jpg;done;' %}


## Dateien runterladen

### Downloads mit curl

{% include alert terminal='wget https://archive.org/compress/kpu001' %}


### WordPress runterladen, entpacken und Archiv löschen

{% include alert terminal='wget http://wordpress.org/latest.tar.gz && tar xfz latest.tar.gz && rm -f latest.tar.gz' %}



## Sonderzeichen eingeben

Die Tilde, also <kbd>~</kbd>, gibt man mit der Tastenkombination <kbd>Alt</kbd> + <kbd>n</kbd> gefolgt von einmal anschließend <kbd>Leertaste</kbd> drücken.

Das Backslash-Zeichen <kbd>\</kbd> erhalten Sie, wenn Sie <kbd>Umschalten</kbd> + <kbd>Alt</kbd> + <kbd>7</kbd> drücken.

Die geschwungenen Klammern <kbd>{</kbd> und <kbd>}</kbd> liegen auf den normalen Klammern. Über die Tastatur geben Sie diese mit <kbd>alt</kbd> + <kbd>8</kbd> oder <kbd>9</kbd> ein.





 [1]: http://support.apple.com/kb/HT2531?viewlocale=de_DE&locale=de_DE
 [2]: #
 [3]: #
 [4]: #
 [5]: #
 [6]: #
 [7]: #
 [8]: #
 [9]: #
 [10]: #


</div><!-- /.medium-7.columns -->
</div><!-- /.row -->
