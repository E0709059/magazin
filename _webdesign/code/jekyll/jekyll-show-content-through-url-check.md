---
layout: page
subheadline: "Jekyll Code Schnipsel"
title: "Check via URL which content to show"
teaser: ""
permalink: /code/jekyll/content-by-url/
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
If you want to check against an exact URL use `==`.

{% highlight ruby %}
{% raw %}{% if page.url == "/ticket.html" %}{% endraw %}
<!-- content here -->
{% raw %}{% endif %}{% endraw %}
{% endhighlight %}

If you don’t want to use an exact URL choose `contains` instead.

{% highlight ruby %}
{% raw %}{% if page.url contains "ticket.html" %}{% endraw %}
<!-- content here -->
{% raw %}{% endif %}{% endraw %}
{% endhighlight %}



Source: <http://wolfslittlestore.be/2013/10/jekyll-includes-tip-contains/>