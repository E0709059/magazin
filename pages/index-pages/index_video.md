---
layout: page
title: Video
teaser: "Phlow.TV erklärt in unterhaltsamen und professionellen Video-Anleitungen schnell und unkompliziert, wie Sie Webdesign, Social Media, Software und Hardware optimal nutzen."
permalink: /video/
collection: video
---
[Phlow.TV auf YouTube ›](https://www.youtube.com/user/PhlowMedia/)
{: .button.radius.success }

[Phlow.TV abonnieren ›](http://www.youtube.com/subscription_center?add_user=phlowmedia)
{: .button.radius.success }


<ul class="no-bullet">
{% for phlow_tv in site.phlow_tv %}
<li class="clearfix">
<h2><a href="{{ site.url }}{{ phlow_tv.url }}">{{ phlow_tv.title }}</a>
</h2>
<p>{% if phlow_tv.image.thumb %}<a href="{{ site.url }}{{ phlow_tv.url }}"><img class="left" src="{% if phlow_tv.image.thumb contains 'http' %}{{ phlow_tv.image.thumb }}{% else %}{{ site.urlimg }}{{ phlow_tv.image.thumb }}{% endif %}" alt="" width="228"></a>{% endif %}{{ phlow_tv.teaser }} <a href="{{ site.url }}{{ phlow_tv.url }}">Anschauen ›</a></p>
</li>
{% endfor %}
</ul>