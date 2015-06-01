---
layout: page
breadcrumb: true
title: "IF – Wenn Metadaten vorhanden, dann ausgeben"
teaser: "IF-Abfragen eignen sich hervorragend, um Daten zu filtern. Um mit einer IF-Abfrage zu prüfen, ob die Variable vorhanden ist, ist das folgende Code-Schnipsel hilfreich."
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
## Einfache IF-Abfrage

{% highlight html %}
{% raw %}
{% if page.author %}
    {{ page.author }}
{% endif %}
{% endraw %}
{% endhighlight %}


## IF-Abfrage mit ELSE-Alternative

{% highlight html %}
{% raw %}
{% if page.author %}
    {{ page.author }}
{% else %}
    Für diesen Beitrag gibt es keine Autoreninformationen
{% endif %}
{% endraw %}
{% endhighlight %}



## Mehrere IF-Abfragen mit ELSIF

Die folgende Abfrage liest sich als Befehl wie folgt: Wenn es eine `page.meta_title`-Variable gibt, dann gib den Inhalt aus. Wenn nicht, dann gib den `page.title` aus. Gibt es auch diese Variable nicht, dann greif bitte auf die `site.title`-Variable zurück.

{% highlight html %}
{% raw %}
<title>
{% if page.meta_title %}{{ page.meta_title }}
{% elsif page.title %}{{ page.title }}
{% else %}{{ site.title }}
{% endif %}</title>
{% endraw %}
{% endhighlight %}
