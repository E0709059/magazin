---
#
# Use the widgets beneath and the content will be
# inserted automagically in the webpage. To make
# this work, you have to use › layout: frontpage
#
layout: frontpage
title: "Phlow Magazin – Webdesign, Journalismus &amp; Social Media"
header:
    image_fullwidth: header_workspace.jpg
---
<div class="row">
  <div class="medium-4 columns">
    <h4 class="b15">Social Media Specials</h4>
    <ul class="side-nav">
      {% for page in site.pages reversed %}
      {% if page.tags contains 'social media' && 'plattform' %}<li><a href="{{ site.url }}{{ page.url }}">{{ page.title }}</a></li>{% endif %}
      {% endfor %}
      <li>&nbsp;</li>
    </ul>
  </div><!-- /.medium-4.columns -->


  <div class="medium-4 columns">
    <h4 class="b15">Videoanleitungen</h4>
    <ul class="side-nav">
      {% for phlow_tv in site.phlow_tv | limit:5 %}
      <li><a href="{{ site.url }}{{ phlow_tv.url }}"><strong>{{ phlow_tv.title }}</strong></a></li>
      {% endfor %}
      <li>&nbsp;</li>
    </ul>
  </div><!-- /.medium-4.columns -->


<div class="medium-4 columns">
    <h4 class="b15">Interviews</h4>
    <p>
      Unsere Interviews befragen Webdesigner, Programmierer, Netzexperten, Blogger und Journalisten zu Themen rund um das Thema <em>digitales Publizieren</em>.
    </p>

    <ul class="side-nav">
      {% for interview in site.interview %}
      <li><a href="{{ site.url }}{{ interview.url }}">{{ interview.title }}</a></li>
      {% endfor %}
      <li>&nbsp;</li>
    </ul>
</div><!-- /.medium-4.columns -->
</div><!-- /.row -->


<div class="row">
<div class="medium-4 columns">
</div><!-- /.medium-4.columns -->


  <div class="medium-4 columns">
    <h4 class="b15">Glossare</h4>
    <ul>
      {% for page in site.pages %}
      {% if page.tags contains 'glossar' %}<li><a href="{{ site.url }}{{ page.url }}">{{ page.title }}</a></li>{% endif %}
      {% endfor %}
    </ul>
</div><!-- /.medium-4.columns -->


<div class="medium-4 columns">
</div><!-- /.medium-4.columns -->
</div><!-- /.row -->



<div class="t30 b60" style="padding: 30px 0; background: #4b4b4d;">

<div class="row">
  <div class="small-12 text-center medium-10 medium-offset-1 columns">
    <h2 style="color: #fff;" class="shadow-black b30">Auf dem Laufenden bleiben und keine Anleitungen und Tipps verpassen.</h2>
    <a class="radius button success shadow-black" href="#" data-reveal-id="newsletter-abo">Den Phlow Magazin Newsletter abonnieren ›</a>
  </div><!-- /.small-12 medium-8.columns -->
</div><!-- /.row -->
</div>





<div id="newsletter-abo" class="reveal-modal" data-reveal>
  <iframe width="800" height="720" src="http://phlow.us2.list-manage1.com/subscribe?u=acb99fb0411d067a7c7ccdb61&id=81e932aa5d" frameborder="0" allowfullscreen=""></iframe>
  <a class="close-reveal-modal">&#215;</a>
</div>

