---
layout: page
subheadline: "Jekyll Code Schnipsel"
title: "List Your Posts by Tags"
teaser: ""
permalink: /code/jekyll/list-posts-by-tags/
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

## Listing all Tags

{% highlight ruby %}
{% raw %}
<ul class="tags">
{% for tag in site.tags %}
  {% assign t = tag | first %}
  {% assign posts = tag | last %}
  <li>{{t | downcase | replace:" ","-" }} has {{ posts | size }} posts</li>
{% endfor %}
</ul>
{% endraw %}
{% endhighlight %}



## Listing all Tags and the posts containing that Tag

{% highlight ruby %}
{% raw %}
{% for tag in site.tags %}
  {% assign t = tag | first %}
  {% assign posts = tag | last %}

{{ t | downcase }}
<ul>
{% for post in posts %}
  {% if post.tags contains t %}
  <li>
    <a href="{{ post.url }}">{{ post.title }}</a>
    <span class="date">{{ post.date | date: "%B %-d, %Y"  }}</span>
  </li>
  {% endif %}
{% endfor %}
</ul>
{% endfor %}
{% endraw %}
{% endhighlight %}


Source: [www.jokecamp.com](http://www.jokecamp.com/blog/listing-jekyll-posts-by-tag/)
