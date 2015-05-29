---
layout: page
breadcrumb: true
title: "For Loop: Posts und Pages mit Kategoriennamen ausgeben"
teaser: "Code-Schnipsel, um Beiträge mit Kategoriennamen auszugeben."
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
Den Kategoriennamen eines Beitrages gibt man mit `{% raw %}{{ post.categories }}{% endraw %}` aus. Da ein Beitrag auch in mehreren Kategorien einsortiert werden kann, schnappt sich im unteren Beispiel der Parameter `first` lediglich die erste Kategorie. Anschließend verwandelt der zweite Parameter `capitalize` den Kategoriennamen so um, dass der erste Buchstabe der Kategorie großgeschrieben wird. Der Befehl sieht dann so aus: `{% raw %}{{ post.categories | first | capitalize }}{% endraw %}`


## Die komplette For-Loop mit Ausgabe der Kategorie

{% highlight html %}
{% raw %}
<ul class="disc">
    {% for post in site.posts %}
    <li>
        <span class="category-name">{{ post.categories | first | capitalize }}</span>
        <a href="{{ site.url}}/{{ post.url }}">{{ post.title }}</a>
    </li>
    {% endfor %}
</ul>
{% endraw %}
{% endhighlight %}
