---
layout: page
breadcrumb: true
title: "IF – Wenn Metadaten vorhanden, dann ausgeben"
teaser: "Um mit einer IF-Abfrage zu prüfen, ob die Variable vorhanden ist, ist das folgende Code-Schnipsel hilfreich."
date:   2014-05-27 00:00:00
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

{% highlight html %}
{% raw %}
{% if page.author %}
    {{ page.author }}
{% endif %}
{% endraw %}
{% endhighlight %}

{% highlight html %}
{% raw %}
{% if page.meta %}
    {{ page.meta }}
{% endif %}
{% endraw %}
{% endhighlight %}


