---
layout: page
breadcrumb: true
title:  "Bilder einbauen mit dem Plugin Jekyll Image Tag"
header:
    image: code_shutterstock_225068266.png
    background-color: "#900055"
    caption: »Flat design vector concept« von Shutterstock
    caption_url: http://www.shutterstock.com/pic.mhtml?id=225068266&src=id
image:
    thumb: icon/icon-jekyll.svg
style: "#masthead-with-background-color { padding: 0; }"
categories:
    - code
tags:
    - jekyll
    - liquid
    - rezept
    - code

---
Mit Hilfe des Jekyll Plugins [jekyll-image-tag][1] verkleinert und vergrößert man automatisch Bilder. Damit das Jekyll Image Tag funktioniert benötigt man:

* [Jekyll](http://jekyllrb.com) `>=1.0`
* [Minimagick](https://github.com/minimagick/minimagick) `>=3.6`
* [Imagemagick](http://www.imagemagick.org/script/index.php)

Denn Minimagick und Imagemagick übernehmen die eigentliche Aufgabe der Bildbearbeitung.


## Jekyll Image Tag installieren

Nachdem man das [Plugin über Github heruntergeladen][1] hat, kopiert man die `image_tag.rb`-Datei in den Jekyll Plugins-Ordner `_plugins`. Ist der Plugins-Ordner noch nicht vorhanden ist, erstellt man diesen einfach im Jekyll-Projekt-Verzeichnis.


## Voreinstellungen (Presets) in _config.yml definieren

Bevor man das Jekyll Image Tag nutzen kann, müssen erst Voreinstellungen, die Presets, in der `_config.yml`-Datei eingegeben werden. Diese benötigt das Plugin, um die Quelldateien zu finden, um diese anschließend anhand von Parametern zu verkleinern oder zu vergrößern.

{% highlight yaml %}
image:
  source: assets/images/_fullsize
  output: generated
  presets:
    users:
      attr:
        class: user-portrait
        itemprop: image
      width: 350
    half:
      width: 400
      height: 400
{% endhighlight %}



## Bilder einbauen mit dem Jekyll Image Tag

Das Liquid-Tag sieht wie folgt aus:

<code>&#123;% image [preset or WxH] path/to/img.jpg class="alignleft" %&#125;</code>

Dabei kann man dem Tag entweder eine vordefinierte Größe als Parameter übergeben oder direkte Pixelangaben machen. Will man z.B. nur die Breite bestimmen und die Höhe soll proportional angepasst werden, gibt man anstelle eines Pixelwertes den Parameter `auto` an. Das sieht dann so aus:

<code>&#123;% image 300xauto path/to/img.jpg class="alignleft" %&#125;</code>



## Bilder einbauen mit Liquid-Variablen

<code>&#123;% image {{ post.featured_image }} alt="our project" %&#125;</code>

{% raw %}
~~~
{% image poster.jpg alt="The strange case of Dr. Jekyll" %}
{% image gallery poster.jpg alt="The strange case of Dr. Jekyll" class="gal-img" data-selected %}
{% image 350xAUTO poster.jpg alt="The strange case of Dr. Jekyll" class="gal-img" data-selected %}
~~~
{% endraw %}

 <code>&#123;% image &#123;&#123; post.featured_image &#125;&#125; alt="\&#123;\&#123; user_name &#125;&#125;" %&#125;</code>


 [1]: https://github.com/robwierzbowski/jekyll-image-tag
 [2]: #
 [3]: #
 [4]: #
 [5]: #
 [6]: #
 [7]: #
 [8]: #
 [9]: #
 [10]: #