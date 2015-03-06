---
layout: page
subheadline: "#2 Aufbau Phlow Magazin"
title: Mehr Inhalte importiert
teaser: "Damit das Phlow Magazin schnell einen Mehrwert bietet, importiere ich zur Zeit alte Inhalte und aktualisiere diese."
categories: blog
---
## Neu: Über Phlow Magazin-Text

Die *Über/Info-*Webseite gehört zu den wichtigsten Orientierungspunkten für Besucher, wenn Sie sich näher über die Webseite erfahren wollen, auf der sie sich gerade befinden. Darum habe ich mich heute morgen als erstes an den [»Eine Quelle für Webdesigner, Journalisten & Blogger«]({{ site.url }}/info/) gesetzt. Der Text beschreibt den *Auftrag*, welchem sich das Phlow Magazin verschrieben hat.


## Import: Interviews

In den nächsten Monaten plane ich kontinuierlich Interviews mit Webdesignern, Social Media-Experten, Bloggern und Journalisten zu den verschiedensten Themen zu veröffentlichen. Einen ersten Anfang für die Interview-Kollektion machen vier alte Interviews aus der Reihe »Wie wichtig sind Blogs für die Gesellschaft?«.

<ul>
{% for interview in site.interview %}
{% if interview.title contains "Gesellschaft" %}<li><a href="{{ site.url }}{{ interview.url }}">{{ interview.title }}</a></li>{% endif %}
{% endfor %}
</ul>