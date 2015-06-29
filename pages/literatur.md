---
layout: page-fullwidth
subheadline: "Journalismus – Webdesign – Social Media"
title: "Literatur"
teaser: "Empfehlenswerte Literatur aus den Bereichen Journalismus, Webdesign, Social Media und Design. Verlinkte Buchtitel bieten eine Rezension auf Phlow Magazin."
permalink: /literatur/
header: no
tags:
    - Literatur
    - Deutsch
    - Englisch
---
<div class="row">
<div class="medium-6 columns" markdown="1">

<h2>Deutsche Titel</h2>

<ul class="no-bullet">
{% for book in site.data.literatur %}
    {% if book.language == empty %}
    {% elsif book.language contains 'Deutsch' %}
        <li class="b30">
            <span class="font-size-h5">
                {% if book.review_url contains = 'http' %}
                    <a href="{{ book.review_url }}">»{{ book.title }}«</a>
                {% elsif book.review_url %}
                    <a href="{{ site.url }}{{ book.review_url }}">»{{ book.title }}«</a>
                {% else %}»{{ book.title }}«{% endif %}
            </span><br>
            Autor: {{ book.author | join: ', '}}<br>
            {% if book.publisher %}Verlag: {{ book.publisher }}{% if book.date_published %}, {{ book.date_published }}{% endif %}<br>{% endif %}
            {% if book.isbn %}ISBN: {{ book.isbn }}<br>{% endif %}
            {% if book.download_link %}<a href="{{ book.download_link }}">Kostenloser Download</a><br>{% endif %}
            {% if book.website %}<a href="{{ book.website }}">Website zum Buch</a><br>{% endif %}
            {% if book.tags %}Schlagworte: {{ book.tags | join: ', '}}<br>{% endif %}
            {% if book.review_url %}<a href="{{ book.review_url }}">Buchbesprechung</a><br>{% endif %}
            {% if book.amazon_link %}<a target="_blank" class="t15 button radius tiny" href="{{ book.amazon_link }}">Bei Amazon kaufen ›</a><br>{% endif %}
        </li>
    {% endif %}
{% endfor %}
</ul>



</div><!-- /.medium-6.columns -->
<div class="medium-6 columns" markdown="1">

<h2>Englische Titel</h2>

<ul class="no-bullet">
{% for book in site.data.literatur %}
    {% if book.language == empty %}
    {% elsif book.language contains 'Englisch' %}
        <li class="b30">
            <span class="font-size-h5">
                {% if book.review_url contains = 'http' %}
                    <a href="{{ book.review_url }}">»{{ book.title }}«</a>
                {% elsif book.review_url %}
                    <a href="{{ site.url }}{{ book.review_url }}">»{{ book.title }}«</a>
                {% else %}»{{ book.title }}«{% endif %}
            </span><br>
            Autor: {{ book.author | join: ', '}}<br>
            {% if book.publisher %}Verlag: {{ book.publisher }}{% if book.date_published %}, {{ book.date_published }}{% endif %}<br>{% endif %}
            {% if book.isbn %}ISBN: {{ book.isbn }}<br>{% endif %}
            {% if book.download_link %}{{ book.download_link }}<br>{% endif %}
            {% if book.download_link %}<a href="{{ book.download_link }}">Kostenloser Download</a><br>{% endif %}
            {% if book.website %}<a href="{{ book.website }}">Website zum Buch</a><br>{% endif %}
            {% if book.tags %}Schlagworte: {{ book.tags | join: ', '}}<br>{% endif %}
            {% if book.review_url %}<a href="{{ book.review_url }}">Buchbesprechung</a><br>{% endif %}
            {% if book.amazon_link %}<a target="_blank" class="t15 button radius tiny" href="{{ book.amazon_link }}">Bei Amazon kaufen ›</a><br>{% endif %}
        </li>
    {% endif %}
{% endfor %}
</ul>




</div><!-- /.medium-6.columns -->
</div><!-- /.row -->

