---
layout: page
breadcrumb: true
title: "For Loop: Inhalte filtern und ausgeben"
teaser: "Die Reihenfolge von Posts innerhalb einer For-Loop dreht man mit dem Parameter reversed um."
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

## Den Inhalt einer For-Loop umdrehen mit *reversed*

{% highlight html %}
{% raw %}
<ul>
	{% for post in site.posts reversed %}
	<li><a href="{{ site.url }}{{ post.url }}">{{ post.title }}</a></li>
	{% endfor %}
	<li>&nbsp;</li>
</ul>
{% endraw %}
{% endhighlight %}


## Wie nutze ich eine IF ELSE-Anweisung innerhalb einer Schleife, wenn keine Posts in einer Kategorie sind?

Der Trick liegt in der Abfrage, ob eine Kategorie keine Einträge hat. Das geschieht mit:


{% highlight html %}
{% raw %}
	{% if site.categories.webdesign == null %}
{% endraw %}
{% endhighlight %}


### Die komplette for-loop

{% highlight html %}
{% raw %}
{% if site.categories.webdesign == null %}
	<p>Es gibt leider keine Beiträge</p>
{% else %}
	{% for post in site.categories.webdesign %}
	<article>
		<h3><a href="{{ post.permalink }}">{{ post.title }}</a></h3>
		<p>{{ post.summary }}</p>
	</article>
	{% endfor %}
{% endif %}
{% endraw %}
{% endhighlight %}

<small>Quelle: [How do I create an IF ELSE statement if there are no Jekyll posts in a category?](http://stackoverflow.com/questions/23923416/how-do-i-create-an-if-else-statement-if-there-are-no-jekyll-posts-in-a-category)</small>

