---
layout: page
subheadline: Jekyll
title: For Loop
teaser: "Diese For-Schleife findet zuerst alle Kategorien und arbeitet sie ab. Die zweite For-Schleife – innerhalb der ersten – schaut sich alle <em>posts</em> an, die zu dieser Kategorie gehören. Der if-Befehl filtert die <em>posts</em> heraus, die das Layout <em>post</em> haben (angegeben im front matter)."
header: no
---
{% highlight ruby %}
<ul>
{% for category in site.categories %}
  <li>
    <strong>{{ category | first }}</strong>
    <ul>
    {% for posts in category %}
    {% for post in posts %}
    {% if post.layout == "post" %}
        <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endif %}
    {% endfor %}
    {% endfor %}
    </ul>
  </li>
{% endfor %}
</ul>
{% endhighlight %}
