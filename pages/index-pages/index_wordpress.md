---
layout: page-fullwidth
title: WordPress
teaser: "WordPress ist das weltweit beliebteste Redaktionssystem, mit welchem Sie leicht eine Website aufbauen und betreuen können. Ob als Firmen-Website, Profil-Seite, Blog oder für Ihr Geschäft: <strong>WordPress ist ein Allroundtalent.</strong> Eine Programmiersprache müssen Sie nicht lernen. Denn die Konstruktion der Website übernimmt WordPress. Das Phlow Magazin hilft Ihnen bei der <a href='{{ site.url }}/video/wordpress-installation/'>Installation</a> und stellt Ihnen die besten <a href='{{ site.url }}/wordpress/plugins/'>WordPress Erweiterungen</a> und <a href='{{ site.url }}/wordpress/themes/'>Themes</a> vor."
image:
    thumb: icon/icon-wordpress.svg
header:
    image: icon/wordpress-logo-498x113.png
    background-color: "#82cbd0"
style: "#navigation > nav > section > ul.left > li.active > a { background: #82cbd0; color: #fff; }"
permalink: /wordpress/
show_meta: false
---

<div class="row">
<div class="small-6 columns" markdown="1">

Die Schwerpunkte von WordPress bilden Ästhetik, Webstandards und Benutzerfreundlichkeit. WordPress ist kostenlos nutzbar und einfach zu installieren. WordPress ermöglicht Ihnen einen professionellen Webauftritt.



## Artikel

{% include list-collection.html collection='wordpress' %}


## Videos

<ul class="side-nav">
  {% for page in site.phlow_tv %}
    {% if page.url contains 'wordpress' %}
    <li><a href="{{ site.url }}{{ page.url }}">{{ page.title }}</a></li>
    {% endif %}
  {% endfor %}
  <li>&nbsp;</li>
</ul>

</div><!-- /.small-6.columns -->
<div class="small-6 columns" markdown="1">
<h2 style="margin-top: 0;">Das WordPress-Buch</h2>

[![]({{ site.urlimg }}wordpress-buch-2.jpg)][3]

<a style="background: #82cbd0;" class="shadow-black button radius" href="http://www.amazon.de/gp/product/3955618609/ref=as_li_tl?ie=UTF8&camp=1638&creative=19454&creativeASIN=3955618609&linkCode=as2&tag=phlow-21&linkId=2MZKAARU43DMJ637">Bei Amazon kaufen ›</a>
<a style="background: #82cbd0;" class="shadow-black button radius" href="{{ site.url }}/wordpress/buch/">Mehr zum Buch ›</a>

## Installation von WordPress

<div class="flex-video"><iframe width="1280" height="720" src="https://www.youtube.com/embed/lW820hNkXrI" frameborder="0" allowfullscreen></iframe></div><!-- /.flex-video -->

<a style="background: #82cbd0;" class="shadow-black button radius" href="{{ site.url }}/video/wordpress-installation/">Mehr Informationen ›</a>


## Dateien hochladen mit dem FTP-Programm Filezilla

<div class="flex-video"><iframe width='970' height='546' src='//www.youtube.com/embed/ystpUgSaPrA' frameborder='0' allowfullscreen></iframe></div><!-- /.flex-video -->


[Mehr Informationen ›][2]
{: .button.radius.success }


</div><!-- /.small-6.columns -->
</div><!-- /.row -->


 [1]: {{ site.url }}/video/wordpress-installation/
 [2]: {{ site.url }}/video/filezilla/
 [3]: {{ site.url }}/wordpress/buch/
 [4]: #
 [5]: #
 [6]: #
 [7]: #
 [8]: #
 [9]: #
 [10]: #