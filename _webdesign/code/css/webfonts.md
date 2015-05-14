---
layout: page
subheadline: "Webfonts einbinden"
title: "CSS-Befehl für den Einbau von Schriften"
teaser: "Wenn Sie eine Schrift auf einer Website einbauen wollen, die nicht zu den Standardschrift gehört, benötigen Sie den Befehl <code>@font-face</code>."
tags:
    - css
breadcrumb: true
---
Über diesen bindet man die unterschiedlichen Schrift-Formate *eot*, *woff*, *truetype* oder *svg* für die verschiedenen Browser ein. Die Webfonts sucht der Browser dann unter der jeweils angegebenen Adresse.

{% highlight css %}
@font-face{ 
    font-family: 'MyWebFont';
    src: url('WebFont.eot');
    src: url('WebFont.eot?iefix') format('eot'),
         url('WebFont.woff') format('woff'),
         url('WebFont.ttf') format('truetype'),
         url('WebFont.svg#webfont') format('svg');
}
{% endhighlight %}
