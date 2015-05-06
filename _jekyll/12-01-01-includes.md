---
layout: page
title: "Includes (mit Parametern)"
teaser: ""
header:
    image: logo-jekyll.png
    background-color: "#333333"
image:
    thumb: icon/icon-jekyll.svg
chapter: "12"
permalink: /jekyll/includes/
breadcrumb: true
---
Quelle für die folgenden Parameter siehe unten Links.


* [Code-Schnipsel: »Jekyll includes tip: contains«](http://wolfslittlestore.be/2013/10/jekyll-includes-tip-contains/)


## Include parameters


{% raw %}
    {% include button-group.html param='flr' %}
{% endraw %}

{% raw %}
<div class="button-group {% if include.param == 'flr' %}pull-right{% endif %}">
    <button>Button 1</button>
    <button>Button 2</button>
    <button>Button 3</button>
</div>
{% endraw %}


{% raw %}
{% include button-group.html modifier='pull-right' %}
{% endraw %}

{% raw %}
<div class="button-group {{ include.modifier }}">
    <button>Button 1</button>
    <button>Button 2</button>
    <button>Button 3</button>
</div>
{% endraw %}

{% raw %}
{% include read-later.html modifier='pull-right' digit=223 %}
{% endraw %}

{% raw %}
<span class="read-later {{ include.modifier }}">
    {% if include.digit %}
        {{ include.digit }}
    {% else %}
        456
    {% endif %}
</span>
{% endraw %}


 [1]: http://bengie.github.io/some-kind-of-workflow/#/3/2
 [2]: http://bengie.github.io/some-kind-of-workflow/#/3/3
 [3]: http://bengie.github.io/some-kind-of-workflow/#/3/4
 [4]: #
 [5]: #
 [6]: #
 [7]: #
 [8]: #
 [9]: #
 [10]: #