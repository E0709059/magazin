---
layout: page
title:  "Erste Schritte zum eigenen Jekyll-Theme"
teaser: "Der einfachste Weg mit einem neuen CMS eine eigene Website zu bauen, ist die Modifizierung des bestehenden Themes. Das pure Standard-Jekyll-Theme eignet sich gut als Ausgangspunkt für die ersten Schritte."
header:
    image: logo-jekyll.png
    background-color: "#333333"
image:
    thumb: icon/icon-jekyll.svg
chapter: "4"
permalink: /jekyll/jekyll-theme/
breadcrumb: true
---

Die Jekyll-Layout-Dateien liegen im Ordner `_layouts` und umfassen die Dateien `default.html`, `post.html` und `page.html`. Welches Layout für eine Seite genutzt wird, definiert man im so genannten [Front-Matter][1].

Das Front-Matter ist der Bereich zu Beginn eines Beitrages, der die Metadaten zum jeweiligen Dokument zusammenfasst. Die Blog-Beiträge findet man im Verzeichnis `_posts`.



## includes – Wiederkehrende Code-Teile auslagern

Auch Jekyll erlaubt das zerlegen eines Templates in verschiedene Bauteile. Für die Übersicht zerlegen Sie am Besten Ihr bestehendes Theme in vier Bestandteile:

1. header
2. footer
3. sidebar
4. content

Da sich *content* aus dem Inhalt der Textdateien ergibt, kümmern Sie sich  zuerst um die ersten drei Bauteile. Dazu legen Sie einen Ordner *_includes* an, in welchem Sie die folgenden drei Dateien anlegen:

1. *header.html*
2. *footer.html*
3. *sidebar.html*

Innerhalb eines Templates ruft man diese Code-Bauteile über den Befehl {% raw %}`{% include code-teil.html %}`{% endraw %} auf. Zum Beispiel: {% raw %}`{% include footer.html %}`{% endraw %}.

Anschließend öffnen Sie das *default.html*-Template und kopieren den oberen Teil bis {% raw %}`{{ content }}`{% endraw %} in *header.html* und den abschließenden Teil nach {% raw %}`{{ content }}`{% endraw %} in *footer.html*.

Um die *includes* innerhalb von *default.html* aufzurufen, genügt der Befehl {% raw %}`{% include header.html %}`{% endraw %}. Die *default.html*-Datei sieht dann so aus:

{% highlight html %}{% raw %}
{% include header.html %}
    {{ content }}
{% include footer.html %}
{% endraw %}{% endhighlight %}





 [1]: {{ site.url }}/jekyll/front-matter/
 [2]: #
 [3]: #
