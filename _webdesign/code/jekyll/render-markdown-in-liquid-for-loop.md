---
layout: page
breadcrumb: true
subheadline: "Jekyll Code Schnipsel"
title: "Render Markdown in Liquid For Loop"
teaser: ""
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

## YAML

{% highlight ruby %}
additional_sidebar:
  - editorial-extra.md
  - editorial-extra-2.md
{% endhighlight %}



## For Loop spitting out the sidebar

{% highlight ruby %}
{% raw %}
{% for sidebar in page.additional_sidebar %}
  {% capture sidebarmd %}{% include {{ sidebar }} %}{% endcapture %}
  <section class="aside">
    {{ sidebarmd | markdownify }}
  </section>
{% endfor %}
{% endraw %}
{% endhighlight %}



Source: [Stackoverflow](http://stackoverflow.com/questions/25914243/render-markdown-specified-in-jekyll-liquid-for-loop)
