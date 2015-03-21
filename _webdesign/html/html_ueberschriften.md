---
published: false
layout: page
title: "Überschriften, Untertitel und Zwischenüberschriften"
teaser: "Mithilfe der Überschriften-Tags lassen sich Texte nicht nur optisch gliedern, sondern Sie übergeben mit diesen Tags gleichzeitig auch eine Gewichtung."
categories:
    - html
---
Wörter, Begriffe und Sätze, die Sie als Hauptüberschrift ausweisen, haben eine höhere Priorität als Abschnittsüberschriften. Wichtig ist diese Tatsache vor allem bei der maschinellen Auslesung und Weiterverarbeitung, wenn Webseiten von Suchmaschinen gelesen werden.

Beson­dere Bedeutung messen die Suchmaschinenalgorithmen dabei strukturierenden Ele­menten bei, z.B. den Überschriften-Tags. Somit hilft der Einsatz von Überschriften nicht nur Ihren Lesern bei der Orientierung, sondern auch den Suchrobotern von Google & Co

Normalerweise bekommt ein Artikel eine Überschrift (Headline), längere Artikel strukturiert man zusätzlich mit Untertitel (Subheadline) und weiteren Zwischenüber­schriften. Besonders die Zwischenüberschriften gliedern den Text thematisch.

Bei HTML-Dokumenten stehen Ihnen dafür die Headline-Elemente `<h1>` bis `<h6>` zur Verfügung. Das Tag `<h1>` steht dabei für die Überschrift höchster Rangordnung, auf die die restlichen Tags hierarchisch folgen. Für jede HTML-Datei können Sie nur ein `<h1>`-Tag nutzen. Mehrere `<h2>` bis `<h6>`-Tags sind erlaubt. Dieses Konzept verfolgt die Logik eines Buches oder eines Artikels. Denn auch ein Buch oder ein Artikel hat nur einen Titel, kann aber verschiedene Unterkapitel besitzen

Für unseren kleinen Artikel über das Onlinespiel Samorost benutzen wir eine Überschrift sowie einen erklärenden Untertitel. Da es kein eigenes Element für Unter­titel gibt, weisen wir die Subheadline mit dem `<h2>`-Element aus. Beide Tags werden, wie auch alle restlichen Tags, innerhalb des `<body>-Tags platziert:

{% highlight html %}
<body>
<h1>Flashspiel: Samorost 2</h1>
<h2>Liebevoll gestaltetes Adventure-Game mit Humor</h2>
</body>
{% endhighlight %}

