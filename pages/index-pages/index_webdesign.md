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
    <div class="medium-6 columns">
        <h2>HTML5 & CSS LERNEN</h2>
        <div class="flex-video"><iframe width="1280" height="720" src="https://www.youtube.com/embed/videoseries?list=PL_9q18jtRBgGzsAZ6cSjz35Gvz8VxtDSh" frameborder="0" allowfullscreen=""></iframe></div>
        <p>Schritt für Schritt lernst Du HTML und CSS. Darüberhinaus stelle ich Dir wichtige Werkzeuge und Software für die Arbeit als Webdesigner vor.</p>
        <p><a class="radius button medium" href="https://www.youtube.com/watch?v=_P9hcbMrnpk&feature=youtu.be&list=PL_9q18jtRBgGzsAZ6cSjz35Gvz8VxtDSh/" target="_blank">Serie auf YouTube anschauen ›</a></p>


    </div><!-- /.medium-6.columns -->


    <div class="medium-6 columns">

        <h2>Videos: HTML & CSS Lernen</h2>
        <ul class="side-nav">
        {% assign counter = 1 %}
        {% for page in site.webdesign %}
        {% if page.published == false %}
        {% elsif page.categories contains 'html' and counter < 25 %}
        <li><a href="{{ site.url }}{{ page.url }}">{{ page.title }}</a></li>
        {% assign counter=counter | plus:1 %}
        {% endif %}
        {% endfor %}
        <li></li>
        </ul>

    </div><!-- /.medium-6.columns -->
</div><!-- /.row -->



<div class="row">

    <div class="medium-6 columns">

        <h2>Artikel</h2>
        <ul class="side-nav">
        {% assign counter = 1 %}
        {% for page in site.webdesign %}
        {% if page.published == false %}
        {% elsif page.tags contains 'artikel' and counter < 15 %}
        <li><a href="{{ site.url }}{{ page.url }}">{{ page.title }}</a></li>
        {% assign counter=counter | plus:1 %}
        {% endif %}
        {% endfor %}
        </ul>

        <h2>Buchtipps</h2>
        <ul class="side-nav">
        {% for book in site.data.literatur %}
            {% if book.category contains "Webdesign" %}
                {% if book.review_url %}
                    <li>
                        <a href="{{ book.review_url }}">{{ book.language }} | »{{ book.title }}«</a>
                    </li>
                {% endif %}
            {% endif %}
            {% if forloop.last %}<li class="b30"></li>{% endif %}
        {% endfor %}
        </ul>
    </div><!-- /.medium-6.columns -->


    <div class="medium-6 columns">
        <h2><a href="{{ site.url }}/code/">Code-Schnipsel</a></h2>
        <p>Seit Jahren entwickeln wir Websites. Dabei nutzen wir bestimmte Bausteine immer wieder. Sei es wiederkehrende Webdesign-Elemente in HTML, CSS oder Javascript oder Bausteine für die Entwicklung von WordPress oder Jekyll-Themes. Die hier versammelten Rezepte haben sich alle bewährt.</p>
        <ul class="side-nav">
            <li><a href="{{ site.url }}/code/jekyll/">Jekyll</a></li>
            <li><a href="{{ site.url }}/code/css/">CSS</a></li>
            <li><a href="{{ site.url }}/code/wordpress/">WordPress</a></li>
            <li><a href="{{ site.url }}/code/html/">HTML</a></li>
            <li><a href="{{ site.url }}/code/javascript/">Javascript</a></li>
            <li><a href="{{ site.url }}/code/php/">PHP</a></li>
            <li><a href="{{ site.url }}/code/gulp/">Gulp</a></li>
            <li><a href="{{ site.url }}/code/ruby-on-rails/">Ruby On Rails</a></li>
            <li>&nbsp;</li>
        </ul>

    </div><!-- /.medium-6.columns -->



</div><!-- /.row -->

