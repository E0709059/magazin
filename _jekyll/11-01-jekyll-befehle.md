---
layout: page
title: "Jekyll-Befehle: Aktualisieren, Hilfe aufrufen, Importieren..."
teaser: "Dieses Tutorial erklärt die wichtigsten Jekyll-Befehle für die Konsole, um z.B. Jekyll zu aktualisieren, oder ein Blog zu importieren."
header:
    image: logo-jekyll.png
    background-color: "#333333"
image:
    thumb: icon/icon-jekyll.svg
chapter: "9"
permalink: /jekyll/befehle/
breadcrumb: true
---
## Jekyll aktualisieren

Erscheint eine neue Version von Jekyll, sollte man schleunigst Jekyll auf den neuesten Stand bringen. Um herauszufinden, welche Version auf dem System installiert ist, ruft man einfach Jekyll mit dem Parameter `-v` für Version auf.

{% include alert terminal='jekyll -v' %}

Aktualisiert wird Jekyll dann mit.

{% include alert terminal='sudo gem update jekyll' %}
