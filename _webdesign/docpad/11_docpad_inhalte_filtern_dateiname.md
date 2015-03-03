---
layout: default
icon: docpad.png
title:  "Inhalte filtern nach Dateinamen"
subtitle: ""
description: "Code-Schnipsel für DocPad, das sämtliche Dokumente durchsucht und die Dokumente nach Name sortiert zurückgibt."
date: 2013-10-01
tags:
  - docpad
---
Der untere Code durchsucht die Collection *sortpages*, pickt alle mit *docpad* markierten Dokumente heraus und sortiert diese anschließend über `[{filename:1}]` nach Dateinamen alphabetisch. Um die Reihenfolge umzukehren ändert man die *1* in *-1*

<pre><code class="lang-ruby">
<ul>
<% for page in @getCollection("sortpages").findAll({tags: '$in': 'docpad'}, [{filename:1}]).toJSON(): %>
    <li><a href="<%= doc.url %>"><%= doc.title %></a></li>
<% end %>
</ul>
</code></pre>