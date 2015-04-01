---
layout: page-fullwidth
subheadline: Rezepte für Programmierer
title: Code
teaser: "Seit Jahren entwickeln wir Websites. Dabei nutzen wir bestimmte Bausteine immer wieder. Sei es wiederkehrende Webdesign-Elemente in HTML, CSS oder Javascript oder Bausteine für die Entwicklung von WordPress oder Jekyll-Themes. Die hier versammelten Rezepte haben sich alle bewährt. Nutzen auch Sie dieses Reservoir."
permalink: /code/
header: no
show_meta: false
---
<div class="row">
    <div class="medium-4 columns">
        <h2>Jekyll</h2>
        <ul class="side-nav sans">
          {% for page in site.webdesign %}
          {% if page.published == false %}
          {% elsif page.tags contains 'jekyll' %}
          <li><span><a href="{{ site.url }}{{ page.url }}">{{ page.title }}</a></span></li>
          {% endif %}
          {% endfor %}
          <li>&nbsp;</li>
      </ul>
  </div><!-- /.medium-4.columns -->


  <div class="medium-4 columns">
        <h2>Javascript</h2>
        <ul class="side-nav sans">
          {% for page in site.webdesign %}
          {% if page.published == false %}
          {% elsif page.tags contains 'javascript' %}
          <li><span><a href="{{ site.url }}{{ page.url }}">{{ page.title }}</a></span></li>
          {% endif %}
          {% endfor %}
          <li>&nbsp;</li>
      </ul>
  </div><!-- /.medium-4.columns -->


<div class="medium-4 columns">
        <h2>WordPress</h2>
        <ul class="side-nav sans">
          {% for page in site.webdesign %}
          {% if page.published == false %}
          {% elsif page.tags contains 'wordpress' %}
          <li><span><a href="{{ site.url }}{{ page.url }}">{{ page.title }}</a></span></li>
          {% endif %}
          {% endfor %}
          <li>&nbsp;</li>
      </ul>
</div><!-- /.medium-4.columns -->
</div><!-- /.row -->


<div class="row">
<div class="medium-4 columns">
        <h2>HTML</h2>
        <ul class="side-nav sans">
          {% for page in site.webdesign %}
          {% if page.published == false %}
          {% elsif page.tags contains 'html' %}
          <li><span><a href="{{ site.url }}{{ page.url }}">{{ page.title }}</a></span></li>
          {% endif %}
          {% endfor %}
          <li>&nbsp;</li>
      </ul>
</div><!-- /.medium-4.columns -->


<div class="medium-4 columns">
        <h2>CSS</h2>
        <ul class="side-nav sans">
          {% for page in site.webdesign %}
          {% if page.published == false %}
          {% elsif page.tags contains 'css' %}
          <li><span><a href="{{ site.url }}{{ page.url }}">{{ page.title }}</a></span></li>
          {% endif %}
          {% endfor %}
          <li>&nbsp;</li>
      </ul>
</div><!-- /.medium-4.columns -->


<div class="medium-4 columns">
        <h2>PHP</h2>
        <ul class="side-nav sans">
          {% for page in site.webdesign %}
          {% if page.published == false %}
          {% elsif page.tags contains 'php' %}
          <li><span><a href="{{ site.url }}{{ page.url }}">{{ page.title }}</a></span></li>
          {% endif %}
          {% endfor %}
          <li>&nbsp;</li>
      </ul>
</div><!-- /.medium-4.columns -->
</div><!-- /.row -->

