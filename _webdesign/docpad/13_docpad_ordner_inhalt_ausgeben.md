---
layout: default
icon: docpad.png
title:  "Inhalte eines definierten Ordners ausgeben"
subtitle: ""
description: "Code-Schnipsel für DocPad, das sämtliche Dokumente eines Ordners – hier »Seminare« ausgibt."
date: 2013-10-01
tags:
  - docpad
---
<pre><code class="lang-ruby">
<dl>
<% for post in @getFilesAtPath("seminare").toJSON(): %>
    <dt><a href="<%= post.url %>"><%= post.title %></a></dt>
    <dd><%= post.subtitle %> // <%= post.description %></dd>
<% end %>
</dl>
</code></pre>