---
layout: page-fullwidth
subheadline: "Static Website Generator"
title: "Was ist Jekyll?"
meta_title: "Was ist Jekyll? Und was ist ein Static Website Generator?"
teaser: "Einführung in Jekyll. Dieser Artikel erklärt die Funktionsweise sowie die Pro und Cons des kostenlosen Website Generators von GitHub."
header:
    image: logo-jekyll.png
    background-color: "#333333"
image:
    thumb: icon/icon-jekyll.svg
chapter: "1"
permalink: /jekyll/was-ist-jekyll/
breadcrumb: true
---
<div class="row top-60">
<div class="medium-7 columns" markdown="1">

[Jekyll][1] ist ein so genannter *Static Website Generator*. Das Kommandozeilenprogramm bietet keine [WYSIWYG][2]-Oberfläche, sondern Sie starten Jekyll über die Kommandozeile – z.B. über das [Terminal][5] beim Mac.

Jekyll baut statische HTML-Webseiten anhand von einfachen Textdateien, die eingelesen werden. Dabei handelt es sich um Layout-Dateien und Inhaltsdateien. Jekyll generiert aufgrund der Layout-Vorlagen die statischen HTML-Webseiten. Das funktioniert sogar live während der Entwicklung, da Jekyll einen eigenen Server mitbringt, den Sie samt Jekyll starten können.

Das in Ruby geschriebene Programm eignet sich hervorragend für den Betrieb eines Blog oder für kleine Website-Projekte, wie z.B. Portfolios, Minisites oder kleine Image-Websites.

> Website generators like Jekyll work by combining template files with content and rendering them to static html pages. They provide the best balance between content creation and editing flexibility, serving an incredibly fast and reliable website.

Die Stärken liegen auf der Hand: Da Jekyll nur statische Webseiten generiert, entstehen keine Sicherheitslücken auf dem Server. Außerdem man muss kein Redaktionssystem samt Plugins pflegen, denn Jekyll baut die Website auf dem eigenen Rechner, die man  anschließend per FTP-Programm nur noch hochladen muss. So entfallen Wartungsarbeiten, wie sie z.B. beim [CMS WordPress][3] kontinuierlich anfallen.

> I was originally going to name it Conveyor (because the project was to take one type of file and conveyor belt it through a process that turned it into another format), but I think that was already taken as a gem name. So I thought about it and decided that the most important feature was the ability to transform files of a rather bland format into files that were so much more interesting. This transformation process reminded me of the story of Dr Jekyll and Mr Hyde, and the name jekyll was available as a gem and seemed to encapsulate the ideas of transformation that I wanted. Thus: Jekyll was born!
> <cite><a href="https://talk.jekyllrb.com/t/why-is-jekyllrb-called-jekyll/267">Tom Preston-Werner</a></cite>


## Die Stärken eines Static Website Generators

Jekyll bietet als Static Website Generator zahlreiche Vorteile, die Systeme wie WordPress einfach nicht bieten können. Die wichtigsten Vorteile von Jekyll sind:

* Kaum Serverlast durch statische HTML-Seiten
* Schnelle Performance der Website für gute Suchmaschinenpositionen
* Sicherheit der Webpräsenz dank reinem HTML
* Texte schreibt man im eigenen Lieblingseditor
* Sehr flexible Gestaltung von Templates
* Einfache Entwicklung und Pflege
* Versionskontrolle durch kontinuierliche Backups
* Unkomplizierter Umzug von Websites
* Software- und Formatunabhängigkeit


 [1]: http://jekyllrb.com/
 [2]: http://de.wikipedia.org/wiki/WYSIWYG
 [3]: http://phlow.de/wordpress
 [5]: {{ site.url }}/terminal/



</div><!-- /.medium-7.columns -->
<div class="medium-5 columns" markdown="1">
<h3 class="m0">Jekyll Anleitung</h3>
{% include list-collection.html collection='jekyll' %}
</div><!-- /.medium-5.columns -->
</div><!-- /.row -->


<div class="row top-60">
    <div class="small-12 columns text-center">
        <h2>Pro und Contra Jekyll</h2>
    </div><!-- /.small-12.columns -->
</div><!-- /.row -->


<div class="row">
    <div class="medium-6 columns">
        <div style="color: #fff; background: #00792c;" class="panel radius">
            <h3 style="color: #fff;">Vorteile von Jekyll</h3>
            <ul>
                <li style="color: #fff;">Schnelle Performance der Website</li>
                <li style="color: #fff;">Sicherheit der Webpräsenz da reines HTML</li>
                <li style="color: #fff;">Einfache Entwicklung und Pflege</li>
                <li style="color: #fff;">Versionskontrolle durch kontinuierliche Backups</li>
                <li style="color: #fff;">Unkomplizierter Umzug von Websites</li>
                <li style="color: #fff;">Tool- und Formatunabhängigkeit</li>
                <li style="color: #fff;">Sehr flexible Gestaltung von Templates</li>
                <li style="color: #fff;">Texte schreibt man im Lieblingseditor</li>
            </ul>
        </div>
    </div><!-- /.medium-6.columns -->
    
    <div class="medium-6 columns">
        <div style="background: #aa0132;" class="panel radius">
            <h3 style="color: #fff;">Nachteile von Jekyll</h3>
            <ul>
                <li style="color: #fff;">Installation von Jekyll auf dem Rechner kompliziert</li>
                <li style="color: #fff;">Keine grafische Benutzeroberfläche, sondern Befehlszeile</li>
                <li style="color: #fff;">Folgende Kenntnisse sind notwendig:
                    <ul>
                        <li style="color: #fff;">HTML</li>
                        <li style="color: #fff;">CSS</li>
                        <li style="color: #fff;">Javascript</li>
                        <li style="color: #fff;">Markdown</li>
                        <li style="color: #fff;">YAML</li>
                        <li style="color: #fff;">Optional: Ruby</li>
                        <li style="color: #fff;">Optional: Liquid Template Language</li>
                    </ul>
                </li>
                <li style="color: #fff;">Jekyll baut nicht automatisch (Blog-)-Archivseiten</li>
                <li style="color: #fff;">keine Echtzeit-Plugins für Chat, Kalender oder Kommentare o.ä.</li>
            </ul>
        </div>
    </div><!-- /.medium-6.columns -->
</div><!-- /.row -->



<div class="row top-60">
<div class="medium-8 medium-offset-2 end columns" markdown="1">

## Wie funktioniert Jekyll?

Jeykyll arbeitet als Kommandozeilenprogramm und generiert Webseiten anhand von Textdokumenten und Templates. Eine Datenbank benötigt Jekyll nicht, da beim Start von Jekyll sämtliche Projektdateien indiziert werden und die Metainformationen temporär gespeichert werden.

<div class="alert-box info radius" markdown="1">
TIPP: **Ich möchte von WordPress zu Jekyll wechseln, was nun?**

Das beste Werkzeug um alte WordPress-Beiträge in das Jekyll-Format zu konvertieren ist [Exit WP][4]. Die Beiträge konvertiert das Werkzeuge anhand der wordpress.xml-Datei, die man über das WordPress-Backend unter Werkzeuge exportiert.

 [4]: https://github.com/thomasf/exitwp
</div>

</div><!-- /.medium-8 medium-offset-2 end.columns -->
</div><!-- /.row -->


