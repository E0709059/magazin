---
layout: page
title: "Terminal Befehle"
teaser: "Nachschlagewerk: Eine Sammlung der Terminal-Befehle, die man öfters braucht, schnell aber vergisst."
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
permalink: /terminal-befehle/
---


## Ordner- und Datei-Aktionen



**Programme öffnet man aus dem Terminal über…**

{% include alert terminal='open -a "Sublime Text"' %}


**Aktuellen Ordner in Finder öffnen**

{% include alert terminal="open ." %}

**Verzeichnis mit Inhalt löschen**

{% include alert terminal='rm -rf verzeichnisname' %}

**Versteckte Ordner & Dateien mit Terminal anzeigen**

Mit <kbd>ls</kbd> listet man die Dateien in einem Ordner auf. Um auch versteckte Dateien anzeigen zu lassen, muss man den Parameter <kbd>-all</kbd> oder in der Kurzvariante <kbd>-a</kbd> hinzufügen.

{% include alert terminal='ls -a' %}




## Dateien runterladen

**Downloads mit wget**

{% include alert terminal='wget https://archive.org/compress/kpu001' %}


**WordPress runterladen, entpacken und Archiv löschen**

{% include alert terminal='wget http://wordpress.org/latest.tar.gz && tar xfz latest.tar.gz && rm -f latest.tar.gz' %}