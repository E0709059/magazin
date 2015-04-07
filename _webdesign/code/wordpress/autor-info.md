---
layout: page
subheadline: "WordPress Rezepte"
title: "Autoreninfos und Profilbild unter Artikel einfügen"
teaser: "Dieses Code-Snippet zeigt ausführliche Informationen über Autoren samt Links zum Autor unter WordPress-Beiträgen an."
header:
    image: code_shutterstock_225068266.png
    background-color: "#900055"
    caption: »Flat design vector concept« von Shutterstock
    caption_url: http://www.shutterstock.com/pic.mhtml?id=225068266&src=id
image:
    thumb: icon/icon-wordpress.svg
style: "#masthead-with-background-color { padding: 0; }"
categories:
    - code
tags:
    - wordpress
    - rezept
    - code
breadcrumb: true
---
{% highlight php startinline=true %}
<div id="autor-info">
    <a href="<?php the_author_url() ?>" title="Website von Autor <?php the_author() ?>"><img alt="Phlow-Autor <?php the_author() ?>" src="<?php bloginfo('template_directory'); ?>/images/images_user/autor_id_<?php the_author_ID(); ?>.jpg" /></a>
Dieser Artikel wurde am <?php the_time('d.F Y') ?> von <a title="Website von <?php the_author() ?>" href="<?php the_author_url() ?>"><strong><?php the_author() ?></strong></a> geschrieben.
<?php the_author_description() ?>
</div>
{% endhighlight %}
