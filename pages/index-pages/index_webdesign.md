---
layout: page-fullwidth
title: "Webdesign – HTML, CSS & Co."
teaser: "Wie baut man Webseiten? Welche Software brauche ich? Was ist wichtig beim Webdesign? Wie nutzt man HTML und CSS? Und wie funktioniert Responsive Webdesign? Anleitungen rund um das Thema: Websites bauen."
permalink: /webdesign/
header:
    image_fullwidth: "webdesign-shutterstock-227689126.jpg"
    caption: "»Webdesign, Entwicklung, Programmierung« von Shutterstock"
    caption_url: http://www.shutterstock.com/pic.mhtml?id=227689126&src=id
# Don't index these pages dear Google.
collection: webdesign
noindex: true
format: blog-index
---
<div class="row">
    <div class="medium-7 columns">
        <h2>Artikel</h2>
        {% assign counter = 1 %}
        {% for page in site.webdesign %}
        {% if page.published == false %}
        {% elsif page.tags contains 'artikel' and counter < 15 %}
        <h3><a href="{{ site.url }}{{ page.url }}">{{ page.title }}</a></h3>
        <p class="clearfix">{% if page.image.thumb %}<a href="{{ site.url }}{{ page.url }}"><img class="left" src="{{ site.urlimg }}{{ page.image.thumb }}" alt="" width="128" height="128"></a>{% endif %}{{ page.teaser }} <a href="{{ site.url }}{{ page.url }}">Lesen ›</a></p>
        {% assign counter=counter | plus:1 %}
        {% endif %}
        {% endfor %}
    </div><!-- /.medium-7.columns -->


    <div class="medium-5 columns">
        <h2><a href="{{ site.url }}/code/">Code-Schnipsel</a></h2>
        <p>Seit Jahren entwickeln wir Websites. Dabei nutzen wir bestimmte Bausteine immer wieder. Sei es wiederkehrende Webdesign-Elemente in HTML, CSS oder Javascript oder Bausteine für die Entwicklung von WordPress oder Jekyll-Themes. Die hier versammelten Rezepte haben sich alle bewährt.</p>
        <ul class="side-nav">
            <li><a href="{{ site.url }}/code/jekyll/">Jekyll</a></li>
            <li><a href="{{ site.url }}/code/css/">CSS</a></li>
            <li><a href="{{ site.url }}/code/wordpress/">WordPress</a></li>
            <li><a href="{{ site.url }}/code/html/">HTML</a></li>
            <li><a href="{{ site.url }}/code/javascript/">Javascript</a></li>
            <li><a href="{{ site.url }}/code/php/">PHP</a></li>
            <li><a href="{{ site.url }}/code/gulp/">Gulp</a></li>
            <li>&nbsp;</li>
        </ul>    
    </div><!-- /.medium-5.columns -->
</div><!-- /.row -->

