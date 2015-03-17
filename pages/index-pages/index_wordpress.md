---
layout: page-fullwidth
title: WordPress
teaser: "WordPress ist das weltweit beliebteste Redaktionssystem, mit welchem Sie leicht eine Website betreuen und aufbauen können. Ob als Firmen-Website, Profil-Seite, Blog oder für Ihr Geschäft: <strong>WordPress ist ein Allroundtalent.</strong> Eine Programmiersprache müssen Sie nicht lernen. Denn die Konstruktion der Website übernimmt WordPress."
permalink: /wordpress/
header: no
show_meta: false
---

<div class="row">
<div class="small-6 columns" markdown="1">

Die Schwerpunkte von WordPress bilden Ästhetik, Webstandards und Benutzerfreundlichkeit. WordPress ist kostenlos nutzbar und einfach zu installieren. WordPress ermöglicht Ihnen einen professionellen Webauftritt.



## WordPress-Artikel

{% include list-collection.html collection='wordpress' %}


## WordPress-Videos

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

[Bei Amazon kaufen ›](http://www.amazon.de/gp/product/3955618609/ref=as_li_tl?ie=UTF8&camp=1638&creative=19454&creativeASIN=3955618609&linkCode=as2&tag=phlow-21&linkId=2MZKAARU43DMJ637)
{: .button.radius.success }
[Mehr zum Buch ›][3]
{: .button.radius.success }



## Installation von WordPress

<div class="flex-video"><iframe width="1280" height="720" src="https://www.youtube.com/embed/lW820hNkXrI" frameborder="0" allowfullscreen></iframe></div><!-- /.flex-video -->

[Mehr Informationen ›][1]
{: .button.radius.success }


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