---
layout: page
breadcrumb: true
title: "Link zu nächstem/vorherigen Beitrag innerhalb einer Kategorie"
teaser: "Code-Schnipsel, um innerhalb einer Kategorie den nächsten und vorherigen Beitrag (Post) zu verlinken."
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
## Nächster/Vorheriger Artikel (Post) in Kategorie

{% highlight html %}
{% raw %}
{% for post in site.categories.photos %}
        {% if post.url == page.url %}
            {% assign post_index0 = forloop.index0 %}
            {% assign post_index1 = forloop.index %}
        {% endif %}
    {% endfor %}
    {% for post in site.categories.photos %}
        {% if post_index0 == forloop.index %}
            {% assign next_post = post.url %}
        {% endif %}
        {% if post_index1 == forloop.index0 %}
            {% assign prev_post = post.url %}
        {% endif %}
    {% endfor %}
    {% if next_post %}
        <a href="{{ next_post }}">Next Post</a> <br>
    {% endif %}
    {% if prev_post %}
        <a href="{{ prev_post }}">Previous Post</a> <br>
    {% endif %}
{% endraw %}
{% endhighlight %}
