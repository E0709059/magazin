---
layout: page
subheadline: "CSS Code Snippets"
title: "CSS-Schatten für Texte"
teaser: ""
permalink: /code/css/text-shadow/
header:
    image: code_shutterstock_225068266.png
    background-color: "#900055"
    caption: »Flat design vector concept« von Shutterstock
    caption_url: http://www.shutterstock.com/pic.mhtml?id=225068266&src=id
# image:
#     thumb: icon/icon-css.svg
style: "#masthead-with-background-color { padding: 0; }"
categories:
    - code
tags:
    - css
    - code
---
<p style="text-shadow: 0 2px 3px rgba(0,0,0,.4);">Black Shadow</p>
{% highlight css %}
.shadow-black-2   {text-shadow: 0 2px 3px rgba(0,0,0,.4); }
{% endhighlight %}


<p style="text-shadow: rgba(0, 0, 0, 0.498039) 0px 1px 2px;">Black Shadow</p>
{% highlight css %}
.shadow-black   {text-shadow: 0 1px 3px rgba(0, 0, 0, 0.5); }
{% endhighlight %}


<p style="color: #fbaa00; text-shadow: rgba(255, 255, 255, 0.498039) 0px 1px 2px; background: #000;padding: 10px;">White Shadow</p>
{% highlight css %}
.shadow-white   {text-shadow: rgba(255, 255, 255, 0.498039) 0px 1px 2px;}
{% endhighlight %}



{% highlight css %}
.shadow-no    {text-shadow: rgba(0, 0, 0, 0) 0 0 0;}
{% endhighlight %}



{% highlight css %}
.shadow-3 {
   text-shadow: 0 1px 0 #ccc,
               0 2px 0 #c9c9c9,
               0 3px 0 #bbb,
               0 4px 0 #b9b9b9,
               0 5px 0 #aaa,
               0 6px 1px rgba(0,0,0,.1),
               0 0 5px rgba(0,0,0,.1),
               0 1px 3px rgba(0,0,0,.3),
               0 3px 5px rgba(0,0,0,.2),
               0 5px 10px rgba(0,0,0,.25),
               0 10px 10px rgba(0,0,0,.2),
               0 20px 20px rgba(0,0,0,.15);
}
{% endhighlight %}

