---
layout: page
subheadline: "WordPress Themes programmieren"
title:  "WordPress Rezepte"
teaser: ""
permalink: /wordpress/rezepte/
image:
    thumb: wordpress.png
categories:
    - webdesign
tags:
    - wordpress
    - wordpress rezept
    - code
---


## WordPress Rezept: Self Pings vermeiden

Mit diesem kleinen WordPress-Rezept unterbindet man Self Pings bzw. Trackbacks.

Damit WordPress sich nicht selbst über intern verlinkte Webseiten per Trackback einem Self Ping unterzieht, braucht man nur dieses kleine WordPress Rezept in die `functions.php` zu kopieren und untersagt damit WordPress das Self Pinging untersagt. 

{% highlight php %}
/* REMOVE SELF PINGING */
function remove_self_pinging(&$links,&$pung) {
    $self = get_option('siteurl');
    foreach ($links as $link => $data) {
        if (false !== strpos($link,$self))
            unset($links[$link]);
    }
}
add_action('pre_ping','remove_self_pinging',0,2);
/* END REMOVE SELF PINGING */
{% endhighlight %}

Quelle: <http://thesistut.com/2012/disable-self-pings-wordpress/>

## Autoren-Infos ausgeben

Autoreninfos unter WordPress-Beiträgen mit Links, Beschreibung und allem Pipapo anzeigen.

{% highlight php %}
<div id="autor-info">
	<a href="<?php the_author_url() ?>" title="Website von Autor <?php the_author() ?>"><img alt="Phlow-Autor <?php the_author() ?>" src="<?php bloginfo('template_directory'); ?>/images/images_user/autor_id_<?php the_author_ID(); ?>.jpg" /></a>
Dieser Artikel wurde am <?php the_time('d.F Y') ?> von <a title="Website von <?php the_author() ?>" href="<?php the_author_url() ?>"><strong><?php the_author() ?></strong></a> geschrieben.
	<?php the_author_description() ?>
</div>
{% endhighlight %}



## Ausgabe von rel=”category tag” im Theme verhindern

Theme-Entwickler, die gerne ihre HTML-Seiten mit dem <a href="http://validator.w3.org/">W3C Validator</a> validieren, ärgern sich über das von WordPress eingebaute <code>rel=”category tag”</code>. Zum Glück gibt es wieder ein kleines WordPress-Rezept für die <code>functions.php</code>, mit welcher man die Ausgabe unterbindet.

{% highlight php %}
add_filter('the_category', 'add_nofollow_cat'); 
function add_nofollow_cat($text) {$text = str_replace('rel="category tag"', "", $text); return $text;}
{% endhighlight %}

Quelle: <http://blog.maru-design.eu/bereinigung-des-relcategory-tag-in-wordpress-126/>


## Klassen von wp_nav_menu reduzieren

Dieses Code-Schnippsel reduziert die Ausgabe der zahlreichen CSS-Klassen, die WordPress automatisch bei der Generierung einer Navigation dazugibt.

{% highlight php %}
// Clean wp_nav_menu Output
function change_wp_nav_menu_classes($classes, $item) {
    $classes = array_filter( 
        $classes, 
        create_function( '$class', 
                 'return in_array( $class, 
                      array( "current-menu-item", "current-menu-parent" ) );' )
        );
    return array_merge(
        $classes,
        (array)get_post_meta( $item->ID, '_menu_item_classes', true )
        );
    }
add_filter('nav_menu_css_class', 'change_wp_nav_menu_classes', 10, 2);
{% endhighlight %}

Quelle: <http://www.texto.de/?p=1454>