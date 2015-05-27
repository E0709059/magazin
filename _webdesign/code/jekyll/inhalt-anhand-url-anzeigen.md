---
layout: page
breadcrumb: true
subheadline: "Jekyll Code Schnipsel"
title: "Dieses Code-Schnipsel filtert den Inhalt mittels eine IF-Abfrage, in welcher die URL abgefragt und mit einer Variable überprüft wird."
teaser: ""
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
Wenn Sie Inhalte anhand einer exakten URL überprüfen wollen, dann nutzen Sie in der IF-Abfarge `==`.

{% highlight ruby %}
{% raw %}{% if page.url == "/ticket.html" %}{% endraw %}
<!-- content here -->
{% raw %}{% endif %}{% endraw %}
{% endhighlight %}

Wenn Sie nicht die exakte URL abfragen wollen, sondern nur einen Teil der URL überprüfen wollen, nutzen Sie `contains`.

{% highlight ruby %}
{% raw %}{% if page.url contains "ticket.html" %}{% endraw %}
<!-- content here -->
{% raw %}{% endif %}{% endraw %}
{% endhighlight %}



Source: <http://wolfslittlestore.be/2013/10/jekyll-includes-tip-contains/>