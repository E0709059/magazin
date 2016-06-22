---
layout:         page
subheadline:    'Webdesign Grundlagen'
title:          '#017 CSS Schrift nachladen per Link oder @import'
video:          'https://www.youtube.com/watch?v=hTlCFMxDAGo'
categories:     css
permalink:      /webdesign/html/css-schrift-nachladen-import/
---
Ist eine Schrift nicht auf dem Rechner des Besuchers vorhanden, kannst Du diese über den Browser mit dem CSS-Befehl `<link>` oder @import nachladen. Wie, erklärt das Video.
<!--more-->

Zahlreiche freie Schriften – auch für kommerzielle Zwecke – findest Du auf [www.google.com/fonts](https://www.google.com/fonts). Für die Projektseite nutzen wir [Roboto](https://www.google.com/fonts/specimen/Roboto), [Roboto Slab](https://www.google.com/fonts/specimen/Roboto+Slab) und [Roboto Mono](https://www.google.com/fonts/specimen/Roboto+Mono).

## Alle drei Roboto-Schriften einbauen

{% highlight css %}
<link href='https://fonts.googleapis.com/css?family=Roboto:400,400italic,700,700italic|Roboto+Mono:400,700|Roboto+Slab:400,700' rel='stylesheet' type='text/css'>
{% endhighlight %}



{% include alert success='**Übung:** Schau Dir auf <a href="https://www.google.com/fonts">www.google.com/fonts</a> Schriften an, wähle eine aus und bau Sie in Deine Webseiten ein.' %}
