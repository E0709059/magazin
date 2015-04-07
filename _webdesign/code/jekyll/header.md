---
layout: page
breadcrumb: true
title: "Starterkit für den &lt;head&gt;-Bereich"
teaser: "Code-Snippet mit IF-Abfragen für den &lt;head&gt;-Bereich."
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
<!doctype html>
<html class="no-js" lang="{% if site.language == nil %}en{% else %}{{ site.language }}{% endif %}">
<head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>{% if page.title %}{{ page.title }}{% else %}{{ site.title }}{% endif %}</title>
    <link rel="stylesheet" href="{{ site.url }}/assets/css/style.css" }}"> 
    <script src="{{ site.url }}/assets/js/modernizr.js"></script>
    <link href="http://fonts.googleapis.com/css?family=Inconsolata:400,700|Open+Sans:400italic,400,300,700,800" rel="stylesheet" type="text/css">
    <meta name="google-site-verification" content="xP2HDqwZ_-ElcHVrOgy66izmcyyVmmeBC6oY1uAw5ok" />
    <link rel="author" href="https://plus.google.com/u/0/118311555303973066167"/>
</head>
{% endraw %}
{% endhighlight %}
