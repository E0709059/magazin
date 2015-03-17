---
published: false
layout: page
title: "Beiträge zählen und ausgeben"
teaser: "Dieses Code-Schnipsel gibt die Anzahl der bereits veröffentlichten WordPress-Beiträge aus."
image:
    thumb: wordpress.png
tags:
  - wordpress
---
<pre><code class="lang-php">
<?php echo wp_count_posts()->publish; ?>
</code></pre>