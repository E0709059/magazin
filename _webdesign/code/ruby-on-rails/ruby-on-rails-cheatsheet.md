---
layout: page
subheadline: "Grundlegende Rails-Befehle"
title: "Ruby On Rails Cheetsheet"
teaser: "Eine Sammlung häufig genutzter Ruby On Rails-Befehle für noch schnellere Website-Entwicklung mit Rails."
categories:
    - code
    - development
tags:
    - ruby
    - rails
    - ruby on rails
    - web development
    - web entwicklung
header:
    image: code_shutterstock_225068266.png
    background-color: "#900055"
    caption: »Flat design vector concept« von Shutterstock
    caption_url: http://www.shutterstock.com/pic.mhtml?id=225068266&src=id
image:
    thumb: icon/icon-ruby-on-rails-128x.png
style: "#masthead-with-background-color { padding: 0; }"
---

Rails mit einer vorgegebenen Version installieren

{% include alert terminal='gem install rails -v 4.2.2' %}

Neues Rails-Projekt starten

{% include alert terminal='rails new projekt_name' %}


Rails Applikation mit Server starten

{% include alert terminal='rails server' %}

Neues Daten-Modell erzeugen mit `scaffold`.

{% include alert terminal='rails generate scaffold name_daten_modell name:string' %}

Migration starten

{% include alert terminal='bundle exec rake db:migrate' %}

Migration wieder zurück

{% include alert terminal='rake db:rollback STEP=1' %}

