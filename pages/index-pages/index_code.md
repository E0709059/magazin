---
layout: page-fullwidth
subheadline: Rezepte für Programmierer
title: Code
teaser: "Seit Jahren entwickeln wir Websites. Dabei nutzen wir bestimmte Bausteine immer wieder. Sei es wiederkehrende Webdesign-Elemente in HTML, CSS oder Javascript oder Bausteine für die Entwicklung von WordPress oder Jekyll-Themes. Die hier versammelten Rezepte haben sich alle bewährt."
permalink: /code/
header: no
show_meta: false
---
<div class="row">
  <div class="medium-4 columns">
    <h2><img class="left" src="{{ site.urlimg }}icon/icon-jekyll.svg" width="48" height="48">Jekyll</h2>
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
    <h2><img class="left" src="{{ site.urlimg }}icon/icon-css-128x.png" width="48" height="48">CSS</h2>
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
    <h2><img class="left" src="{{ site.urlimg }}icon/icon-wordpress.svg" width="48" height="48">WordPress</h2>
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
    <h2><img class="left" src="{{ site.urlimg }}icon/icon-html-128x.png" width="48" height="48">HTML</h2>
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
    <h2><img class="left" src="{{ site.urlimg }}icon/icon-javascript-128x.png" width="48" height="48">Javascript</h2>
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
    <h2><img class="left" src="{{ site.urlimg }}icon/icon-php.svg" width="48" height="48">PHP</h2>
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


<div class="row">
  <div class="medium-4 columns">
    <h2><img class="left" src="{{ site.urlimg }}icon/icon-gulp-128x.png" width="48" height="48">Gulp</h2>
    <ul class="side-nav sans">
      {% for page in site.webdesign %}
      {% if page.published == false %}
      {% elsif page.tags contains 'gulp' %}
      <li><span><a href="{{ site.url }}{{ page.url }}">{{ page.title }}</a></span></li>
      {% endif %}
      {% endfor %}
      <li>&nbsp;</li>
    </ul>
  </div><!-- /.medium-4.columns -->


  <div class="medium-4 columns">
  </div><!-- /.medium-4.columns -->


  <div class="medium-4 columns">
  </div><!-- /.medium-4.columns -->
</div><!-- /.row -->

