---
layout: page
subheadline: "WordPress Rezepte"
title: "SelfPings vermeiden"
teaser: "Mit diesem kleinen WordPress-Rezept untersagt man WordPress sich mit Self Pings bzw. Trackbacks selbst zu benachrichtigen."
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
Damit WordPress sich nicht selbst über intern verlinkte Webseiten per Trackback einem Self Ping unterzieht, braucht man nur dieses kleine WordPress Rezept in die `functions.php` zu kopieren und untersagt damit WordPress das Self Pinging untersagt. 

{% highlight php startinline=true %}
/* Self Pings Abschalten */
function remove_self_pinging(&$links,&$pung) {
    $self = get_option('siteurl');
    foreach ($links as $link => $data) {
        if (false !== strpos($link,$self))
            unset($links[$link]);
    }
}
add_action('pre_ping','remove_self_pinging',0,2);
/* Ende Self Pings Abschalten */
{% endhighlight %}

Quelle: <http://thesistut.com/2012/disable-self-pings-wordpress/>
