---
published: false
layout: page-fullwidth
subheadline: Theme
title: Data Output
teaser: "Webdesigner versorgen die WordPress-Community kontinuierlich mit neuen Layouts und Design. Von diesen Themes gibt es mittlerweile eine unüberschaubare Anzahl. Phlow Magazin stellt die herausragende Themes vor."
permalink: /wordpress/themes-test/
categories:
    - webdesign
tags:
    - wordpress
    - themes
image:
    thumb: icon/icon-wordpress.svg
header:
    image: icon/wordpress-logo-498x113.png
    background-color: "#82cbd0"
style: "#navigation > nav > section > ul.left > li:nth-child(5) > a { background: #82cbd0; color: #fff; }"
---

{% for theme in site.data.wordpress-themes %}

## {{ theme.name }}






<img src="{{ site.urlimg }}{{ theme.screenshots.url }}" alt="WordPress Theme {{ theme.name }}">

{{ theme.description }}

<a class="button radius success" href="{{ theme.download }}">Download</a>
<a class="button radius success" href="{{ theme.demo }}">Demo</a>
<a class="button radius success" href="{{ theme.anleitung }}">Anleitung</a>



{% endfor %}