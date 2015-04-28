---
layout: page
subheadline: "WordPress Rezepte"
title: "Ausgabe von rel=”category tag” im Theme verhindern"
teaser: 'Theme-Entwickler, die gerne ihre HTML-Seiten mit dem <a href="http://validator.w3.org/">W3C Validator</a> validieren, ärgern sich über das von WordPress eingebaute <code>rel="category tag"</code>. Zum Glück gibt es wieder ein kleines WordPress-Rezept für die <code>functions.php</code>, mit welcher man die Ausgabe unterbindet.'
header:
    image: code_shutterstock_225068266.png
    background-color: "#82cbd0"
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
// Ausgabe von rel="category tag" im Theme verhindern
//
add_filter('the_category', 'add_nofollow_cat'); 
function add_nofollow_cat($text) {
$text = str_replace('rel="category tag"', "", $text);
return $text
}
{% endhighlight %}

Quelle: <http://blog.maru-design.eu/bereinigung-des-relcategory-tag-in-wordpress-126/>