---
layout: default
icon: docpad.png
menutitle: ""
title:  "Gib keinen Inhalt aus, wenn gleich..."
description: "Der Inhalt innerhalb der IF-Anweisung wird *nicht* ausgegeben, wenn der Dokumententitel auf »Phlow UX Design«"
date: 2013-10-01
tags:
  - docpad
---
<pre><code class="lang-ruby">
<%= if @document.title is "Phlow UX Design" then "" else "#{@document.title}" %>
</code></pre>
