---
layout: page
subheadline: "Jekyll Code Schnipsel"
title: "_include to List Posts by Parameters"
teaser: ""
permalink: /code/jekyll/list-posts-parameters/
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
The `list-posts.html`-include is a loop to list posts. It's a helper to add some additional content fast and easy. You can use it in individual posts for example. Which parameters you use, depends on you.

Possible parameter for the loop:

- entries › define the number of entries to show
- offset › define the offset (number of entries to skip before displaying the first one)
- category › define **only one** category to display according entries

The loop looks when you use all parameters. Single parameters are possible of course.

{% highlight ruby %}
{% raw %}{% include list-posts.html entries='3' offset='1' category='design' %}{% endraw %}
{% endhighlight %}



{% highlight ruby %}
{% raw %}
<ul class="side-nav">
  {% if include.categories == NULL %}
    {% for post in site.posts limit:include.entries offset:include.offset %}
      <li><a href="{{ site.url }}{{ post.url }}">{% if post.subheadline %}{{ post.subheadline }} &middot; {% endif %}<strong>{{ post.title }}</strong></a></li>
    {% endfor %}
      <li class="text-right"><a href="{{ site.url }}/blog/archive/"><strong>More ›</strong></a></li>
  {% elsif include.categories != empty %}
  {% assign category = include.categories %}
    {% for post in site.categories.[category] limit:include.entries offset:include.offset %}
      <li><a href="{{ site.url }}{{ post.url }}">{% if post.subheadline %}{{ post.subheadline }} &middot; {% endif %}<strong>{{ post.title }}</strong></a></li>
    {% endfor %}
      <li class="text-right"><a href="{{ site.url }}/blog/archive/"><strong>More ›</strong></a></li>
  {% endif %}
</ul>
{% endraw %}
{% endhighlight %}
