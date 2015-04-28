---
layout: page
subheadline: "WordPress Rezepte"
title: "Klassen von wp_nav_menu reduzieren"
teaser: "Dieses Code-Schnippsel reduziert die Ausgabe der zahlreichen CSS-Klassen, die WordPress automatisch bei der Generierung einer Navigation dazugibt."
header:
    image: code_shutterstock_225068266.png
    background-color: "#82cbd0"
    caption: »Flat design vector concept« von Shutterstock
    caption_url: http://www.shutterstock.com/pic.mhtml?id=225068266&src=id
image:
    thumb: icon/icon-wordpress.svg
style: "#masthead-with-background-color { padding: 0; }"
categories:
    - code
tags:
    - wordpress
    - rezept
    - code
breadcrumb: true
---
{% highlight php startinline=true %}
// wp_nav_menu Output Aufraeumen
//
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