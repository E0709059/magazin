---
layout: page
breadcrumb: true
subheadline: "Jekyll Code Schnipsel"
title: "Tags auflisten mit For-Loop"
teaser: "Diese For-Loop listet alle Tags auf."
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
    - for loop
    - tags
---
Die Tags definiert man im [front-matter][1]-Bereich eines Jekyll-Beitrages mit:

{% include alert terminal='tags: <br>&nbsp;&nbsp;&nbsp;&nbsp;- schlagwort-eins<br>&nbsp;&nbsp;&nbsp;&nbsp;- schlagwort-zwei' %}


{% highlight html %}
{% raw %}
{% for tag in page.tags %}
    <a href="{{ site.url }}/tag/{{ tag | escape }}.html">{{ tag }}</a><br />
{% endfor %}
{% endraw %}
{% endhighlight %}


 [1]: {{ site.url }}/jekyll/front-matter/
