---
layout: page
title: "Texte Schreiben für das Internet"
teaser: Worauf kommt es beim Texten an? Wie schreibe ich eine Nachricht und wie ein Interview? Wie formuliere ich meine Texte für soziale Medien? Welche Werkzeuge und Software bringen mich weiter? Unsere Anleitungen, Videos und Tipps unterstützen Sie beim digitalen Publizieren.
permalink: /text/
header:
    image_fullwidth: header_typewriter.jpg
show_meta: false
---

<ul class="no-bullet">
{% for text in site.text %}
{% unless text.published == false %}
<li class="clearfix">
<h2><a href="{{ site.url }}{{ text.url }}">{{ text.title }}</a>
</h2>
<p>{% if text.image.thumb %}<a href="{{ site.url }}{{ text.url }}"><img class="left" src="{{ site.urlimg }}{{ text.image.thumb }}" alt="" width="128" height="128"></a>{% endif %}{{ text.teaser }} <a href="{{ site.url }}{{ text.url }}">Anschauen ›</a></p>
</li>
{% endunless %}
{% endfor %}
</ul>
