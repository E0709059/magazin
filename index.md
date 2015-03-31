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
    <h4 class="b15"><a href="{{ site.url }}/social-media/">Social Media Specials</a></h4>
    <ul class="side-nav">
      {% for page in site.pages %}
      {% if page.tags contains 'social media special' %}<li><a href="{{ site.url }}{{ page.url }}">{{ page.title }}</a></li>{% endif %}
      {% endfor %}
      <li>&nbsp;</li>
    </ul>
    <h4 class="b15">Marketing Specials</h4>
    {% include list-collection.html collection='marketing' %}
  </div><!-- /.medium-4.columns -->


  <div class="medium-4 columns">
    <h4 class="b15"><a href="{{ site.url }}/phlow-tv/">Videoanleitungen</a></h4>
    {% include list-collection.html collection='phlow_tv' %}
  </div><!-- /.medium-4.columns -->

  <div class="medium-4 columns">
    <h4 class="b15"><a href="{{ site.url }}/webdesign/">Webdesign</a></h4>
    {% include list-collection.html collection='webdesign' %}
  </div><!-- /.medium-4.columns -->


</div><!-- /.row -->


<div class="row">
  <div class="medium-4 columns">
    <h4 class="b15">Bildbearbeitung</h4>
    {% include list-collection.html collection='bild' %}
  </div><!-- /.medium-4.columns -->


  <div class="medium-4 columns">
    <h4 class="b15">Interviews</h4>
    <p>
      Unsere Interviews befragen Webdesigner, Programmierer, Netzexperten, Blogger und Journalisten zu Themen rund um das Thema <em>digitales Publizieren</em>.
    </p>
    {% include list-collection.html collection='interview' %}
  </div><!-- /.medium-4.columns -->


  <div class="medium-4 columns">
    <h4 class="b15">Glossare</h4>
    <ul class="side-nav">
      {% for page in site.pages %}
      {% if page.tags contains 'glossar' %}<li><a href="{{ site.url }}{{ page.url }}">{{ page.title }}</a></li>{% endif %}
      {% endfor %}
      <li>&nbsp;</li>
    </ul>
    
    <div class="border-dotted">{% include ad/google-adsense-responsive %}</div>

  </div><!-- /.medium-4.columns -->
</div><!-- /.row -->



<div class="t30 b60" style="padding: 30px 0; background: #82cbd0;">
<div class="row">
    <div class="small-12 text-center medium-12 columns">
      <a href="#" data-reveal-id="newsletter-abo"><img class="left" src="{{ site.urlimg }}mailchimp-freddie-200x.png" width="200" height="200"></a>
      <h2 class="shadow-black" style="margin: 10px 0; color: #fff;" >Keine Anleitungen und Tipps verpassen: Newsletter abonnieren.</h2>
      <a class="radius button info shadow-black" href="#" data-reveal-id="newsletter-abo">Den Phlow Magazin Newsletter abonnieren ›</a>
    </div><!-- /.small-12 medium-8.columns -->
  </div><!-- /.row -->
</div>



<div id="newsletter-abo" class="reveal-modal" data-reveal>
  <iframe width="100%" height="580" src="http://phlow.us2.list-manage1.com/subscribe?u=acb99fb0411d067a7c7ccdb61&id=81e932aa5d" frameborder="0" allowfullscreen=""></iframe>
  <a class="close-reveal-modal">&#215;</a>
</div>

