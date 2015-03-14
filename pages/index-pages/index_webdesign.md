---
layout: page-fullwidth
title: Webdesign
permalink: /webdesign/
breadcrumb: true
header: no
---
<ul class="side-nav">
  {% for webdesign in site.webdesign %}
    {% if webdesign.published == false %}
    {% else %}
    <li><a href="{{ site.url }}{{ webdesign.url }}">{{ webdesign.title }}</a></li>
    {% endif %}
  {% endfor %}
  <li>&nbsp;</li>
</ul>