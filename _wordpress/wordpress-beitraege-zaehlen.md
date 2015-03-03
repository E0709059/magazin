---
layout: default
icon: wordpress.png
title:  "Beiträge zählen und ausgeben"
subtitle: ""
date: 
description: "Dieses Code-Schnipsel gibt die Anzahl der bereits veröffentlichten WordPress-Beiträge aus."
tags:
  - wordpress
---
<pre><code class="lang-php">
<?php echo wp_count_posts()->publish; ?>
</code></pre>