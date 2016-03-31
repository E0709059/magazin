---
#
# Use the widgets beneath and the content will be
# inserted automagically in the webpage. To make
# this work, you have to use › layout: frontpage
#
layout: frontpage_special_phlow_magazin
title: "Phlow Magazin – Webdesign, Journalismus &amp; Social Media"
header:
    image: start-webdesign-shutterstock-22768912.png
    background-color: "#29aebc"
style: "#masthead-with-background-color { padding: 10px; }"
homepage: true
---
<div class="row">
  <div class="medium-6 columns">
    <a href="{{ site.url }}/social-media/"><img src="{{ site.urlimg }}startseite-social-media-special-thumb.png" width="332" alt="Phlow Video"></a>
    <h4 class="b15"><a href="{{ site.url }}/social-media/">Social Media Specials</a></h4>
    <ul class="side-nav">
      {% for page in site.pages %}
      {% if page.tags contains 'soziales netzwerk' %}<li><a href="{{ site.url }}{{ page.url }}">{{ page.title }}</a></li>{% endif %}
      {% endfor %}
      <li>&nbsp;</li>
    </ul>
    <p class="sans text-right"><a class="button tiny radius" href="{{ site.url }}/social-media/"><strong>Mehr ›</strong></a></p>
  </div><!-- /.medium-6.columns -->

  <div class="medium-6 columns">
    <a href="{{ site.url }}/text/"><img src="{{ site.urlimg }}startseite-text-thumb.png" width="332" alt="Texte schreiben"></a>
    <h4 class="b15"><a href="{{ site.url }}/text/">Texte Schreiben für das Internet</a></h4>
    {% include list-collection-by-tag.html collection='text' tag='darstellungsform' limit='5' %}
    <p class="sans text-right"><a class="button tiny radius" href="{{ site.url }}/text/"><strong>Mehr ›</strong></a></p>
  </div><!-- /.medium-6.columns -->

</div><!-- /.row -->



<div class="t30 b60" style="padding: 30px 0; background: #82cbd0;">
<div class="row">
    <div class="small-12 text-center medium-12 columns">
      <a href="http://magazin.phlow.de/newsletter/"><img class="left" src="{{ site.urlimg }}mailchimp-freddie-200x.png" width="200" height="200" alt="Newsletter"></a>
      <h2 class="shadow-black" style="margin: 10px 0; color: #fff;" >Keine Anleitungen und Tipps verpassen: Newsletter abonnieren.</h2>
      <a class="radius button info shadow-black" href="http://magazin.phlow.de/newsletter/">Den Phlow Magazin Newsletter abonnieren ›</a>
    </div><!-- /.small-12 medium-8.columns -->
  </div><!-- /.row -->
</div>





<div class="row t30">
  <div class="medium-6 columns">
    <a href="{{ site.url }}/webdesign/"><img src="{{ site.urlimg }}startseite-webdesign-thumb.png" width="332" alt="Phlow Video"></a>
    <h4 class="b15"><a href="{{ site.url }}/webdesign/">Webdesign</a></h4>
    <ul class="side-nav">
      {% assign counter = 0 %}
      {% for page in site.webdesign %}
        {% if page.categories contains 'code' or page.published == false %}
        {% elsif counter < 5 %}
        <li><a href="{{ site.url }}{{ page.url }}">{{ page.title }}</a></li>
        {% assign counter=counter | plus:1 %}
        {% endif %}
      {% endfor %}
      <li>&nbsp;</li>
  </ul>
    <p class="sans text-right"><a class="button tiny radius" href="{{ site.url }}/webdesign/"><strong>Mehr ›</strong></a></p>
  </div><!-- /.medium-6.columns -->

  <div class="medium-6 columns">
    <a href="{{ site.url }}/bild/"><img src="{{ site.urlimg }}startseite-bild-thumb.png" width="332" alt="Bild und Bildbearbeitung"></a>
    <h4 class="b15"><a href="{{ site.url }}/bild/">Bildbearbeitung</a></h4>
    {% include list-collection.html collection='bild' %}
    <p class="sans text-right"><a class="button tiny radius" href="{{ site.url }}/bild/"><strong>Mehr ›</strong></a></p>
  </div><!-- /.medium-6.columns -->

</div><!-- /.row -->


<div class="row">
  <div class="medium-6 columns">
    <img src="{{ site.urlimg }}startseite-glossar-thumb.png" width="332" alt="Bild und Bildbearbeitung">
    <h4 class="b15">Glossare</h4>
    <ul class="side-nav">
      {% for page in site.pages %}
      {% if page.tags contains 'glossar' %}<li><a href="{{ site.url }}{{ page.url }}">{{ page.title }}</a></li>{% endif %}
      {% endfor %}
      <li>&nbsp;</li>
    </ul>
  </div><!-- /.medium-6.columns -->



  <div class="medium-6 columns">

    <h4 class="b15">Marketing Specials</h4>
    {% include list-collection.html collection='marketing' %}
  </div><!-- /.medium-6.columns -->
</div><!-- /.row -->

