---
layout: page
subheadline: "WordPress Rezepte"
title: "FTP-Daten in wp-config.php speichern"
teaser: "Nicht immer funktioniert die Funktion automatisches Update über das Redaktionssystem von WordPress. Die FTP-Zugangsdaten können Sie aber unkompliziert in der <em>config.php</em>-Datei speichern."
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
define('FTP_HOST', 'ftp.example.org');
define('FTP_USER', 'username');
define('FTP_PASS', 'password');
//
// Sichere Verbindung festlegen
// Standard: false
//
define('FTP_SSL', true);
{% endhighlight %}

Mehr › <https://codex.wordpress.org/Editing_wp-config.php>