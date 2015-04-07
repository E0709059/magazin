---
layout: page
breadcrumb: true
title: "Kategoriennamen ausgeben"
teaser: "Kategoriennamen im front-matter definieren und in Templates ausgeben."
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

style: "#masthead-with-background-color { padding: 0; }"
categories:
    - code
tags:
    - jekyll
    - liquid
    - rezept
    - code
---
Damit man für Posts Kategoriennamen ausgeben kann, müssen diese zuerst im [front-matter][1] definiert werden. Im unteren Beispiel werden die beiden Kategorien `jekyll` und `code` definiert.

{% highlight html %}
---
layout: post
title:  "Kategorien ausgeben"
categories:
    - jekyll 
    - code 
---
{% endhighlight %}

## Kategoriennamen ausgeben

Damit Jekyll mehrere Kategorienamen nicht einfach ohne Leerzeichen in einem Rutsch ausgibt, benutzt man den Parameter `join: ' , '`. Der Parameter verkettet die Kategoriennamen miteinander durch ein beliebige gewünschte Zeichenfolge. Die vorangestellte `if`-Abfrage stellt sicher, dass überhaupt Kategoriennamen im front-matter angegeben wurden.

{% highlight html %}
{% raw %}
{% if page.categories %}Archiviert unter {{ page.categories | join: ' , ' }}{% endif %}
{% endraw %}
{% endhighlight %}


 [1]: {{ site.url}}/anleitung/front-matter
 [2]: #
 [3]: #
 [4]: #
 [5]: #
 [6]: #
 [7]: #
 [8]: #
 [9]: #
 [10]: #