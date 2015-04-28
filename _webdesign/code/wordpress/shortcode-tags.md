---
layout: page
subheadline: "WordPress Rezepte"
title: "Shortcode Snippet das Beiträge nach Tag ausgibt"
teaser: ""
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
function series_function($atts) {
   extract(shortcode_atts(array(
      'tag' => 'video'
   ), $atts));
   $return_string = '<ul class="square">';
   query_posts(array('orderby' => 'date', 'order' => 'DESC' , 'tag' => $tag));
   if (have_posts()) :
      while (have_posts()) : the_post();
         $return_string .= '<li><a href="'.get_permalink().'">'.get_the_title().'</a></li>';
      endwhile;
   endif;
   $return_string .= '</ul>';
   wp_reset_query();
   return $return_string;
}
add_shortcode('series', 'series_function');
{% endhighlight %}
