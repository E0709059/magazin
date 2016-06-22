---
layout:             page
subheadline:        'Webdesign Grundlagen'
title:              '#001 HTML Schnellstart'
meta_description:   'Um Webseiten zu erstellen, muss Du nichts installieren. Das Video zeigt, wie Du deine ersten Webseiten mit Bordmitteln von Windows, Mac oder Linux baust.'
video:              'https://www.youtube.com/watch?v=_P9hcbMrnpk'
categories:         html
image:              '001-html schnellstart.jpg'
header:             no
permalink:          '/webdesign/html/schnellstart/'
breadcrumb:         true
---
Um Webseiten zu erstellen, muss Du nichts installieren. Das Video zeigt, wie Du deine ersten Webseiten mit Bordmitteln von Windows, Mac oder Linux baust.
<!--more-->

- Um Webseiten zu entwickeln braucht man einen Browser, einen einfachen Texteditor.
    - Empfehlung: [Google Chrome](https://www.google.de/chrome/browser/desktop/)
- Webseiten bestehen aus Text-Dateien, die der Browser interpretiert
- *Seitenquelltext* anzeigen
    - Chrome: rechte Maustaste › *Seitenquelltext anzeigen* wählen
    - Firefox: rechte Maustaste › *Seitenquelltext anzeigen* wählen
    - Internet Explorer: rechte Maustaste › *Quellcode anzeigen* wählen
    - Schneller mit Tastaturkürzel
        - Beispiel: In Chrome Tastenkombination auf dem Mac <kbd>cmd + alt + u</kbd> oder Windows <kbd>Strg + U</kbd>
        - [Mehr Tastaturkürzel für Chrome](https://support.google.com/chrome/answer/157179?hl=de)
- Browser erkennen Webseiten-Dokumente anhand der Endung *.html*
- Die Startseite einer Website benennt man mit *index.html*
- HTML-Befehle nennt man Tags
- Webseiten kann man mit dem einfachsten Texteditor erstellen
    - [Mac › Textedit](https://support.apple.com/de-de/HT2523)
    - [Windows › Editor](http://windows.microsoft.com/de-de/windows/open-notepad#1TC=windows-7)
- Codierung › UTF-8 ([Mehr in der Wikipedia](https://de.wikipedia.org/wiki/UTF-8))
- Textedit (Mac)
    - Einstellungen › Format › Reiner Text
    - Dokument erstellen, in reinen Text umwandeln
- Alle Informationen zum Video in der Kommentarbox oder auf <http://webdesign.phlow.de>



## Beispiel Quelltext

{% highlight html %}
<!doctype html>
<html>
    <head>
        <title>Titel der Webseite</title>
        <meta charset=utf-8>
    </head>
    <body>
        <a href="kontakt.html">Kontaktieren Sie mich</a>, wenn Sie eine Webseite benötigen.
    </body>
</html>
{% endhighlight %}

{% include alert success='**Übung:** Erstelle eine dritte Webseite für das Impressum und benenne die Datei mit *impressum.html*. Bearbeite das &lt;title&gt;-Tag mit Impressum und verlink die neue Webseite mit den beiden anderen.' %}


