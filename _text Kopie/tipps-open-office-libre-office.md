---
layout: page
subheadline: Textverarbeitung
title: "Tricks und Tipps für Open Office/Libre Office"
teaser: "Desöfteren muss man Textdokumente neu formatieren oder verkorkste Texte neu formatieren. Diese kleine Tipps-Sammlung spart Ihnen Zeit und Nerven."
permalink: "/text/tipps-open-office-libre-office/"
categories:
    - text
tags:
    - texteditor
    - textverarbeitung
    - open office
    - libre office
    - software
image:
    thumb: "icon/icon-libre-office-128x.png"
---
<div class="panel radius" markdown="1">
**Inhalt**
{: #toc }
*  TOC
{:toc}
</div>



## Absätze und Textelemente in Open Office verschieben

Mit der Tastenkombination <kbd>Strg</kbd> und <kbd>Alt</kbd> plus den Rauf- und Runter-Pfeiltasten verschiebt man komplette Absätze, Überschriften, Listenelemente und ähnliche Textelemente innerhalb eines Dokumentes.

Ein Anwendungsbeispiel: Um die Elemente einer durchnummerierten Liste nachträglich zu sortieren, setzen Sie die Schreibmarke an eine beliebige Position innerhalb eines Listenelementes. Halten Sie jetzt die Tasten <kbd>Strg</kbd> und <kbd>Alt</kbd> gleichzeitig gedrückt und verschieben Sie das Listenelement über Rauf- und Runter-Pfeiltasten.



## Texte mit Suchen & Ersetzen schnell formatieren

Mit Hilfe der Suchen & Ersetzen-Funktion von Open Office/Libre Office und der Hilfe regulärer Ausdrücke formatieren Sie Artikel schneller und automatisieren Sie lästige sich wiederholende Schritte.

### Wofür braucht man reguläre Ausdrücke?

Mit einem [regulären Ausdruck](http://de.wikipedia.org/wiki/Regul%C3%A4rer_Ausdruck) kann man nach Zeichenfolgen und SteuerZeichen suchen – z.B. Tabulatoren, Zeilenumbrüchen oder Zeilenanfängen. Findet der reguläre Ausdruck die Zeichen, können Sie diese mit Hilfe der Suchen und Ersetzen-Funktion durch andere Zeichen ersetzen.

Reguläre Ausdrücke benutzen Sie in Open Office bzw. Libre Office mit Hilfe der *Suchen & Ersetzen*-Funktion. Mit einem regulären Ausdruck erstellen Sie ein Suchmuster, das Sie durch eine andere Zeichenfolge ersetzen können.

Das bedeutet konkret: **Reguläre Ausdrücke helfen verkorkste Dokumente schnell und unkompliziert zu formatieren, anstelle diese mühsam per Hand zu editieren.**


### Texte mit Suchen und Ersetzen formatieren

![]({{ site.urlimg }}software_suchen-ersetzen-open-office.png)

Texte lassen sich auf vielfältige Weise mit regulären Ausdrücken formatieren. Damit reguläre Ausdrücke als solche erkannt werden, muß im Suchen-Ersetzen-Dialog diese Option aktiviert werden (siehe Screenshot).

*   Ein Absatzende sucht man mit dem regulären Ausdruck: `$`
*   Einsetzen muß man Absatzenden jedoch mit dem regulären Ausdruck: `\n`
*   Eine Zeilenschaltung sucht man mit dem regulären Ausdruck: `\n`


### Beliebiges Zeichen ersetzen

Der `.` steht für genau _ein_ beliebiges Zeichen. Um mehrere beliebige Zeichen zu suchen, nutzt man `..`, `...` und so weiter. Will man eine Zeichenfolge mit beliebig oft Zeichen ersetzen, nutzt man zusätzlich das `*`. Das Sternchen auch _Wildcard_ genannt, erweitert die Suche nach einem beliebigen Zeichen auf die Suche nach unendlich vielen Zeichen: `.*`

**Beispiel:**

`class=".*"`

Gibt man die obige Zeichenfolge in der Open Office _Suchen & Ersetzen_-Funktion ein, sucht Open Office nach der exakten Reihenfolge _class="_ mit einer anschließenden beliebig langen Zeichenfolge, bis die Suche auf die Zeichen _"_ stößt. Anschließend ersetzt die Suchfunktion die gefundene Zeichenfolge durch eine neue gewünschte Zeichenfolge.

Das obige Ergebnis findet z.B. die folgenden verschiedenen Zeichenfolgen:

~~~
class="text-align: center;"
class="color: #fff" style="background: #0f0;"
~~~

### Weiterführende Informationen zu regulären Ausdrücken

*   [Wikipedia: Regulärer Ausdruck](http://de.wikipedia.org/wiki/Regul%C3%A4rer_Ausdruck)
*   [ooowiki.de: Suchen Und Ersetzen/Formatieren](http://www.ooowiki.de/SuchenUndErsetzen/Formatieren)
*   [Anwendungsbereich: Regulärer Ausdruck](http://www.ooowiki.de/Regul%C3%A4rerAusdruck)
*   [Praxisbeispiele für die Anwendung regulärer Ausdrücke](http://www.ooowiki.de/SuchenUndErsetzen/Regul%C3%A4reAusdr%C3%BCcke)
*   [Amazon: Standardwerk "Reguläre Ausdrücke" (O'Reilly Verlag)](http://www.amazon.de/gp/product/3897217201/ref=as_li_ss_tl?ie=UTF8&tag=phlow-21&linkCode=as2&camp=1638&creative=19454&creativeASIN=3897217201)



