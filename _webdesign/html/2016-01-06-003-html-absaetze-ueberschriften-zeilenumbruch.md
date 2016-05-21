---
subheadline:   'Webdesign Grundlagen'
title:         '#003 HTML: Texte gliedern mit &lt;p&gt;, &lt;h1&gt; bis &lt;h6&gt; und &lt;br&gt;'
video:          'https://www.youtube.com/watch?v=54Nd3otI1ds'
categories:     html
image:          'html-absaetze-ueberschriften-zeilenumbruch.jpg'
permalink:      '/html-absaetze-ueberschriften-zeilenumbruch/'
---
Dieses Video stellt die grundlegenden HTML-Befehle für die Gliederung von Text vor: Absätze &lt;p&gt;, Überschriften &lt;h1&gt; bis &lt;h6&gt; und Zeilenumbrüche &lt;br&gt;.
<!--more-->

Mithilfe der Überschriften-Tags lassen sich Texte nicht nur optisch gliedern, sondern Du übergibst mit diesen Tags gleichzeitig auch eine Gewichtung. Das ist wichtig für die Suchmaschinenoptimierung und bessere Sichtbarkeit Deiner Webseiten in Google & Co.

Wörter, Begriffe und Sätze, die Du in der Hauptüberschrift nutzt, haben eine höhere Priorität als Abschnittsüberschriften. Beson­dere Bedeutung messen die Suchmaschinenalgorithmen dabei strukturierenden Ele­menten bei, z.B. den Überschriften-Tags. Somit hilft der Einsatz von Überschriften nicht nur Deinen Lesern bei der Orientierung, sondern auch den Suchrobotern.

Normalerweise bekommt ein Artikel eine Überschrift (Headline), längere Artikel strukturiert man zusätzlich mit Untertitel (Subheadline) und weiteren Zwischenüber­schriften. Besonders die Zwischenüberschriften gliedern den Text thematisch.

{% include alert info='In dem Phlow-Artikel <a href="http://magazin.phlow.de/text/meldung-nachricht-news/">»Wie man eine Nachricht schreibt!«</a> lernst Du worauf es bei guten Beiträgen ankommt.' %}

Bei HTML-Dokumenten stehen Ihnen dafür die Headline-Elemente `<h1>` bis `<h6>` zur Verfügung. Das Tag `<h1>` steht dabei für die Überschrift höchster Rangordnung, auf die die restlichen Tags hierarchisch folgen. Für jede HTML-Datei solltest Du nur ein `<h1>`-Tag nutzen. Mehrere `<h2>` bis `<h6>`-Tags sind erlaubt. Das ist wie bei einem Buch: Es gibt einen Buchtitel, aber mehrere Kapitel. Und Kapitel können – je nach Buch – auch weitere Unterkapitel haben.




## HTML-Befehl &lt;p&gt; markiert Absätze

{% highlight html %}
<p>Ein ganz einfacher Absatz.</p>
{% endhighlight %}

## HTML-Befehle für Überschriften

{% include alert warning='Die &lt;h1&gt;-Überschrift darf nur einmal pro HTML-Dokument genutzt werden.' %}

{% highlight html %}
<h1>Überschrift</h1>
<h2>Zwischenüberschrift</h2>
<h3>Überschrift dritter Ordnung</h3>
<h4>Überschrift vierter Ordnung</h4>
<h5>Überschrift fünfter Ordnung</h5>
<h6>Überschrift sechster Ordnung</h6>
{% endhighlight %}



{% include alert success='**Übung:** Gliedere Dein Impressum mit Absätzen, Überschriften und Zeilenumbrüchen. Öffne die anderen Seiten und gib allen Dokumenten eine &lt;h1&gt;-Überschrift.' %}
