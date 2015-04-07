---
layout: page
breadcrumb: true
title: "Counter für Loops"
teaser: "Ein Counter für eine For-Schleife kann vielfach eingesetzt werden. Zum Beispiel kann man die Anzahl von Artikeln mit einem Counter zählen und auszugeben. Oder erst ab einem bestimmten Wert startet man einen Befehl mit Hilfe einerIF-Abfrage."
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

---
Einen Counter für Loops realisiert man mit Hilfe von `{% raw %}{% assign counter = 1 %}{% endraw %}` und `{% raw %}{% assign counter=counter | plus:1 %}{% endraw %}`.

Während `{% raw %}{% assign counter = 1 %}{% endraw %}` den Counter auf den Wert 1 setzt, erhöht `{% raw %}{% assign counter=counter | plus:1 %}{% endraw %}` den Wert jeweils um 1.

Innerhalb der Schleife kann man dann den Wert des Counters über `{% raw %}{{ counter }}{% endraw %}` ausgeben.

Den Counter-Wert überprüft man mit einer IF-Abfrage z.B. so: `{% raw %}{% if counter == 5 %}{% endif %}{% endraw %}`. Diese Abfrage führt dann Code aus, wenn der Counter bei 5 angekommen ist.


## Code-Beispiel mit For-Loop

{% highlight html %}
{% raw %}
<ul class="side-nav">
	{% assign counter = 1 %}
	{% for post in site.posts reversed %}
		{% if post.categories contains include.list-category %}
		<li><a href="{{ site.url }}{{ post.url }}">#{{ counter }} {{ post.title }}</a></li>
		{% assign counter=counter | plus:1 %} 
		{% endif %}
	{% endfor %}
	<li>&nbsp;</li>
</ul>
{% endraw %}
{% endhighlight %}

Bei den HTML-Elementen handelt es sich um das `side-nav`-Element des [Foundation-Frameworks][1].


 [1]: http://foundation.zurb.com/docs/components/sidenav.html
 [2]: #
 [3]: #
 [4]: #
 [5]: #
 [6]: #
 [7]: #
 [8]: #
 [9]: #
 [10]: #