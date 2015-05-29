---
layout: page
breadcrumb: true
subheadline: "Jekyll Code Schnipsel"
title: "For-Loop: Inhalte einer collection auflisten"
teaser: "Diese For-Loop listet die Inhalte einer collection auf – hier <em>music</em> – und greift auf die Informationen im front matter-Bereich zu."
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
{% raw %}
~~~
{% for album in site.music limit:3 %}
      <li>
        <img src="{{ album.thumbnail-path }}" alt="{{ album.title }}"/>
        <a href="{{ album.url }}">{{ album.title }}</a>
        <p>{{ album.short-description }}</p>
      </li>
{% endfor %}
~~~
{% endraw %}


Source: [Getting Started with Jekyll Collections](http://www.sitepoint.com/getting-started-jekyll-collections/)
