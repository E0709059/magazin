---
layout: page-fullwidth
title: WordPress
teaser: WordPress ist das weltweit beliebteste Redaktionssystem für die Betreuung von Webseiten.
permalink: /wordpress/
breadcrumb: true
header: no
show_meta: false
---

<div class="row">
<div class="small-6 columns" markdown="1">

WordPress ist ein Redaktionssystem mit welchem Sie eine Website betreuen und aufbauen können. Dazu müssen Sie keine Programmiersprache oder HTML lernen. Denn die Konstruktion der Website übernimmt das Redaktionssystem.
Ursprünglich als Redaktionssystem für den Betrieb eines Blogs gedacht, hat sich WordPress in den letzten Jahren zu einem Allroundtalent für die Betreuung von Websites gemausert.

Die Schwerpunkte von WordPress bilden Ästhetik, Webstandards und Benutzerfreundlichkeit. WordPress ist frei als Download erhältlich, einfach zu installieren und ermöglicht einen professionellen Webauftritt.

Ein Grund für den Erfolg von WordPress ist, dass Sie es kostenlose nutzen können und von einem offenen Quellcode profitieren. Diesen dürfen Sie verändern, wie Sie wollen.

Das bedeutet: Sie dürfen mit WordPress machen, was Sie wollen. Ob Blog oder Unternehmens-Website, ob Portfolio oder Magazin, die Möglichkeiten für den Einsatz sind vielfältig dank eines äußerst flexiblen und offenen Systems.

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
<h2 style="margin-top: 0;">Installation von WordPress</h2>

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
 [3]: #
 [4]: #
 [5]: #
 [6]: #
 [7]: #
 [8]: #
 [9]: #
 [10]: #