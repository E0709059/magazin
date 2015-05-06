---
layout: page-fullwidth
subheadline: Static Website Generator
title: "Websites bauen mit Jekyll"
meta_title: "Anleitungen für Jekyll, den Static Website Generator"
teaser: "<a href='http://magazin.phlow.de/jekyll/was-ist-jekyll/'>Jekyll</a> ist ein <em>Static Website Generator</em>, der statische HTML-Webseiten erstellt. Ob Blog oder Website-Projekt, die Stärken liegen auf der Hand: Statische Webseiten bieten keine Sicherheitslücken, die Pflege eines Redaktionssystem entfällt und die Webseiten lassen sich perfekt optimieren. <a href='http://magazin.phlow.de/jekyll/was-ist-jekyll/'>Jekyll kennenlernen › </a>."
header:
    image: logo-jekyll.png
    background-color: "#333333"
image:
    thumb: icon/icon-jekyll.svg
permalink: /jekyll/
breadcrumb: true
show_meta: false
---
<div class="row top-60">
    <div class="medium-7 columns">
        <h2>Jekyll lernen Schritt für Schritt</h2>
        {% include list-collection.html collection='jekyll' %}
    </div><!-- /.medium-6.columns -->

    <div class="medium-5 columns">
        <h2>Jekyll-Code-Rezepte</h2>
        <p>Unsere Jekyll-Rezepte helfen Ihnen bei der Entwicklung eigener Jekyll-Websites. Außerdem lernen Sie auch über die Code-Schnipsel die Programmierung von Jekyll.</p>
        {% include list-collection-by-tag.html collection='webdesign' tag='jekyll' limit='7' url='code' %}
    </div><!-- /.medium-6.columns -->
</div><!-- /.row -->


