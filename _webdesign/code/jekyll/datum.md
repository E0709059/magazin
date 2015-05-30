---
layout: page
breadcrumb: true
title: "Datum eines Jekyll-Beitrages ausgeben"
teaser: "Mit <code>page.date</code> gibt man das Datum eines Beitrages aus. Über Filter überschreibt man die voreingestellte Ausgabe Tag-Monat-Jahr des Datums."
header:
    image: code_shutterstock_225068266.png
    background-color: "#900055"
    caption: »Flat design vector concept« von Shutterstock
    caption_url: http://www.shutterstock.com/pic.mhtml?id=225068266&src=id
image:
    thumb: icon/icon-jekyll.svg
style: "#masthead-with-background-color { padding: 0; }"
categories:
    - code
tags:
    - jekyll
    - liquid
    - rezept
    - code
#
# Das Datum muss unbedingt drinbleiben, damit die Code
# Beispiele funktionieren
#
date: 2008-11-07T13:07:54-08:00
---
{% highlight html %}
{% raw %}{{ page.date | date: "%d.%m.%Y" }}{% endraw %}
{% endhighlight %}

Beispiel: Dieser Beitrag wurde am `{{ page.date | date: "%d.%m.%Y" }}` erstellt.



## Datum nach dem XML Schema 

{% highlight html %}{% raw %}{{ page.date | date_to_xmlschema }}{% endraw %}{% endhighlight %}


Beispiel: `{{ page.date | date_to_xmlschema }}`



## Datum nach dem RFC-822 Format

{% highlight html %}{% raw %}{{ page.date | date_to_rfc822 }}{% endraw %}{% endhighlight %}

Beispiel: `{{ page.date | date_to_rfc822 }}`



Wenn Sie noch mehr über die Formatierung des Datums und auch die Möglichkeiten für eine deutsche Anpassung erfahren möchten, dann hilft ihnen der Artikel [»Jekyll Date Formatting Examples«](http://alanwsmith.com/jekyll-liquid-date-formatting-examples) weiter. Der Artikel deckt alle erdenklichen Möglichkeiten ab, das Datum ihren Wünschen entsprechend zu formatieren.
