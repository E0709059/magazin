---
layout: default
icon: css-logo.png
title: "CSS-Befehl für den Einbau von Schriften"
description: ""
isMenu: true
menutitle: "Webfonts einbinden"
tags:
	- css
---
Um eine zusätzliche Schrift auf einer Website einzubauen, benötigt den Befehl `@font-face`. Über diesen bindet man die unterschiedlichen Schrift-Formate *eot*, *woff*, *truetype* oder *svg* für die verschiedenen Browser ein. Die Webfonts sucht der Browser dann unter der jeweils angegebenen Adresse.

<pre><code class="lang-css">
@font-face{ 
    font-family: 'MyWebFont';
    src: url('WebFont.eot');
    src: url('WebFont.eot?iefix') format('eot'),
         url('WebFont.woff') format('woff'),
         url('WebFont.ttf') format('truetype'),
         url('WebFont.svg#webfont') format('svg');
}
</code></pre>
