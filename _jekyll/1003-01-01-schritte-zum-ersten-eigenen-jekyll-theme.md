---
layout: page
title:  "Erste Schritte zum eigenen Jekyll-Theme"
teaser: "Der einfachste Weg mit einem neuen CMS eine eigene Website zu bauen, ist die Modifizierung des bestehenden Themes."
chapter: "4"
permalink: /jekyll/jekyll-theme/
---
 Das pure Jekyll-Theme eignet sich gut als Ausgangspunkt für die ersten Schritte.

 Die Jekyll-Layout-Dateien liegen im Ordner `_layouts` und umfassen die beiden Dateien `default.html` und `post.html`. Welches Layout für eine Seite genutzt wird, definiert man im so genannten *Front-Matter*.

 Das Front-Matter ist der Bereich zu Beginn eines Beitrages, der die Metadaten zum jeweiligen Dokument zusammenfasst. Die Blog-Beiträge findet man im Verzeichnis `_posts`.

## includes – Wiederkehrende Code-Teile auslagern

Auch Jekyll erlaubt das zerlegen eines Templates in verschiedene Teile. Für die Übersicht zerlege ich als erstes das entstehende Theme in vier Bestandteile:

1. `header`
2. `footer`
3. `sidebar`
4. `content`

Da sich `content` aus dem Inhalt der Textdateien speist, kümmere ich mich zuerst um die ersten drei Teile. Dazu lege ich einen Ordner `_includes` an, in welchem ich wiederum die folgenden drei Dateien anlege:

1. `header.html`
2. `footer.html`
3. `sidebar.html`

Innerhalb eines Templates ruft man diese Code-Teile über den Befehl {% raw %}`{% include code-teil.html %}`{% endraw %} auf. Zum Beispiel: {% raw %}`{% include footer.html %}`{% endraw %}.

Anschließend öffne ich das `default.html`-Template und kopiere den oberen Teil bis {% raw %}`{{ content }}`{% endraw %} in `header.html` und den abschließenden Teil nach {% raw %}`{{ content }}`{% endraw %} in `footer.html`.

Um die *includes* innerhalb von `default.html` aufzurufen, genügt der Befehl {% raw %}`{% include header.html %}`{% endraw %}. Die `default.html`-Datei sieht dann so aus:

{% highlight html %}{% raw %}
{% include header.html %}
    {{ content }}
{% include footer.html %}
{% endraw %}{% endhighlight %}
