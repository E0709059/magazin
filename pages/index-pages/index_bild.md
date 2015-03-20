---
layout: page
title: Bild
teaser: "Erfolgreiche Beiträge brauchen gut aufbereitete Bilder. Ob ein Beitrag auf einer Webseite, in einer App oder in sozialen Netzwerken: optimierte Bildern bekommen mehr Aufmerksamkeit. Diese Anleitungen helfen Ihnen Bilder zu erstellen, zu finden und zu bearbeiten."
permalink: /bild/
header: no
show_meta: false
---

<ul class="no-bullet">
{% for bild in site.bild %}
<li class="clearfix">
<h2><a href="{{ site.url }}{{ bild.url }}">{{ bild.title }}</a>
</h2>
<p>{% if bild.image.thumb %}<a href="{{ site.url }}{{ bild.url }}"><img class="left" src="{{ site.urlimg }}{{ bild.image.thumb }}" alt="" width="128" height="128"></a>{% endif %}{{ bild.teaser }} <a href="{{ site.url }}{{ bild.url }}">Anschauen ›</a></p>
</li>
{% endfor %}
</ul>
