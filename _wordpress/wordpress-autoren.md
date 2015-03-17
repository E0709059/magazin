---
published: false
layout: page
title:  "Autoren-Infos ausgeben"
teaser: "Autoreninfos unter WordPress-Beiträgen mit Links, Beschreibung und allem Pipapo anzeigen."
image:
    thumb: wordpress.png
tags:
  - wordpress
  - wordpress rezept
  - code
---
<pre><code class="lang-php">

 <div id="autor-info">
	<a href="<?php the_author_url() ?>" title="Website von Autor <?php the_author() ?>"><img alt="Phlow-Autor <?php the_author() ?>" src="<?php bloginfo('template_directory'); ?>/images/images_user/autor_id_<?php the_author_ID(); ?>.jpg" /></a>
Dieser Artikel wurde am <?php the_time('d.F Y') ?> von <a title="Website von <?php the_author() ?>" href="<?php the_author_url() ?>"><strong><?php the_author() ?></strong></a> geschrieben.
	<?php the_author_description() ?>
</div>

</code></pre>