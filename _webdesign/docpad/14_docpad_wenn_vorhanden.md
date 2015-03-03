---
layout: default
icon: docpad.png
menutitle: ""
title:  "Gib Inhalt aus, wenn vorhanden"
description: "Der Inhalt innerhalb der IF-Anweisung wird nur ausgegeben, wenn die jeweiligen Metadaten vorhanden sind. Der Inhalt zwischen if und end im unteren Beispiel, wird nur ausgegeben, wenn es Metadaten zum Wert thumbnail gibt."
date: 2013-10-01
tags:
  - docpad
---
<pre><code class="lang-ruby">
<% if @document.thumbnail: %>
    <img src="/images/<%= @document.thumbnail %>" alt="">
<% end %>
</code></pre>
