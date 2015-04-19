---
layout: page
subheadline: "WordPress Rezepte"
title: "Beiträge zählen und ausgeben"
teaser: "Dieses Code-Schnipsel gibt die Anzahl der bereits veröffentlichten WordPress-Beiträge aus."
header:
    image: code_shutterstock_225068266.png
    background-color: "#900055"
    caption: »Flat design vector concept« von Shutterstock
    caption_url: http://www.shutterstock.com/pic.mhtml?id=225068266&src=id
image:
    thumb: icon/icon-wordpress.svg
style: "#masthead-with-background-color { padding: 0; }"
categories:
    - code
tags:
    - wordpress
    - rezept
    - code
breadcrumb: true
---
{% highlight php startinline=true %}
<?php echo wp_count_posts()->publish; ?>
{% endhighlight %}
