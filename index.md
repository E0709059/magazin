---
#
# Use the widgets beneath and the content will be
# inserted automagically in the webpage. To make
# this work, you have to use › layout: frontpage
#
layout: frontpage
title: "Phlow Magazin – Webdesign, Journalismus &amp; Social Media"
header:
    title: " "
    image_fullwidth: "header_unsplash_12.jpg"
---
<div class="row">
  <div class="small-12 text-center medium-10 medium-offset-1 columns">
    <h2 class="b30">Verpasse nicht den offiziellen Start des Phlow Magazins und trage Dich in den Phlow-Newsletter ein.</h2>
    <a class="radius button success" href="#" data-reveal-id="newsletter-abo">Phlow Newsletter ›</a>
  </div><!-- /.small-12 medium-8.columns -->
</div><!-- /.row -->

<hr class="t30">

<div class="row">
  <div class="medium-4 columns">
    <h4>Glossare</h4>
    <ul>
      {% for page in site.pages %}
      {% if page.tags contains 'glossar' %}<li><a href="{{ site.url }}{{ page.url }}">{{ page.title }}</a></li>{% endif %}
      {% endfor %}
    </ul>

  </div><!-- /.medium-4.columns -->
  <div class="medium-4 columns">
    <h4>Interviews</h4>
    <p>
      Unsere Interviews befragen Webdesigner, Programmierer, Netzexperten, Blogger und Journalisten zu Themen rund um das Thema <em>digitales Publizieren</em>.
    </p>

    <ul>
      {% for interview in site.interview %}
      <li><a href="{{ site.url }}{{ interview.url }}">{{ interview.title }}</a></li>
      {% endfor %}
    </ul>
  </div><!-- /.medium-4.columns -->
  <div class="medium-2 columns"></div><!-- /.medium-2.columns -->
</div><!-- /.row -->

<hr class="t30">



<div id="newsletter-abo" class="reveal-modal" data-reveal>
  <iframe width="800" height="720" src="http://phlow.us2.list-manage1.com/subscribe?u=acb99fb0411d067a7c7ccdb61&id=81e932aa5d" frameborder="0" allowfullscreen=""></iframe>
  <a class="close-reveal-modal">&#215;</a>
</div>
