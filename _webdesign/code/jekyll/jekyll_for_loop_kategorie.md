---
layout: page
subheadline: "Jekyll Code Schnipsel"
title: "For Loop"
teaser: "Diese For-Schleife findet zuerst alle Kategorien und arbeitet sie ab. Die zweite For-Schleife – innerhalb der ersten – schaut sich alle <em>posts</em> an, die zu dieser Kategorie gehören. Der if-Befehl filtert die <em>posts</em> heraus, die das Layout <em>post</em> haben (angegeben im front matter)."
permalink: /code/jekyll/for-loop/
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
{% highlight ruby %}
<ul>
 {% raw %}{% for category in site.categories %}{% endraw %}
  <li>
    <strong>{% raw %}{{ category | first }}{% endraw %}</strong>
    <ul>
    {% raw %}{% for posts in category %}{% endraw %}
    {% raw %}{% for post in posts %}{% endraw %}
    {% raw %}{% if post.layout == "post" %}{% endraw %}
        <li><a href="{% raw %}{{ post.url }}{% endraw %}">{% raw %}{{ post.title }}{% endraw %}</a></li>
    {% raw %}{% endif %}{% endraw %}
    {% raw %}{% endfor %}{% endraw %}
    {% raw %}{% endfor %}{% endraw %}
    </ul>
  </li>
{% raw %}{% endfor %}{% endraw %}
</ul>
{% endhighlight %}
