---
layout: page-fullwidth
title: "Texte Schreiben für das Internet"
teaser: Worauf kommt es beim Texten an? Wie schreibe ich eine Nachricht und wie ein Interview? Wie formuliere ich meine Texte für soziale Medien? Welche Werkzeuge und Software bringen mich weiter? Unsere Anleitungen, Videos und Tipps unterstützen Sie beim digitalen Publizieren.
permalink: /text/
header:
    image_fullwidth: header_typewriter.jpg
collection: text
---
<div class="row">
    <div class="medium-7 columns">
        <h2>Texten Schreiben</h2>
        {% assign counter = 1 %}
        {% for page in site.text %}
        {% if page.published == false %}
        {% elsif page.tags contains 'darstellungsform' and counter < 15 %}
        <h3><a href="{{ site.url }}{{ page.url }}">{{ page.title }}</a></h3>
        <p class="clearfix">{% if page.image.thumb %}<a href="{{ site.url }}{{ page.url }}"><img class="left" src="{{ site.urlimg }}{{ page.image.thumb }}" alt="" width="128" height="128"></a>{% endif %}{{ page.teaser }} <a href="{{ site.url }}{{ page.url }}">Lesen&nbsp;›</a></p>
        {% assign counter=counter | plus:1 %}
        {% endif %}
        {% endfor %}
    </div><!-- /.medium-7.columns -->


    <div class="medium-5 columns">
        <h2>Buchempfehlungen</h2>
        <ul class="side-nav">
        {% for page in site.text %}
            {% if page.tags contains 'buchkritik' %}
            <li><a href="{{ site.url }}{{ page.url }}">{{ page.title }}</a></li>
          {% endif %}
        {% endfor %}
        <li></li>
        </ul>

        <h2>Journalismus</h2>
        <ul class="side-nav">
        {% for page in site.text %}
            {% unless page.published == false %}
                {% unless page.tags contains 'darstellungsform' %}
                    {% unless page.tags contains 'buchkritik' %}
                    <li><a href="{{ site.url }}{{ page.url }}">{{ page.title }}</a></li>
                    {% endunless %}
              {% endunless %}
            {% endunless %}
        {% endfor %}
        <li></li>
        </ul>
    </div><!-- /.medium-5.columns -->
</div><!-- /.row -->

