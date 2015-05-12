---
layout: page
subheadline: "WordPress Rezepte"
title: "Autoreninfos und Profilbild unter Artikel einfügen"
teaser: "Dieses Code-Snippet zeigt ausführliche Informationen über Autoren samt Links zum Autor unter WordPress-Beiträgen an. Zusätzlich bietet es die Möglichkeit ein individuelles Autorenbild zu nutzen."
header:
    image: code_shutterstock_225068266.png
    background-color: "#82cbd0"
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
    - autor
breadcrumb: true
---

Von Haus aus legt WordPress für jeden Autor/Teilnehmer ein eigenes Profil an. Mit diesen Daten des Autorenprofil können Sie ober- oder unterhalb des Beitrages Informationen zum Autor anzeigen. Das personalisiert den jeweiligen Beitrag und macht besonders bei einem Weblog mit mehreren Autoren Sinn.

## Autorenbilder für WordPress-Einträge

Das WordPress-Benutzerprofil beinhaltet Felder für Namen, Nick, URL, Kurzbeschreibung und verschiedene Instant-Messenger-IDs. Wichtig und schön ist neben den Autoreninformationen jedoch auch ein Portrait bzw. ein kleines Avatar-Bild. Will man nicht auf den Gravatar-Service zurückgreifen, ist man erst einmal aufgeschmissen, da es keinen Bilder-Upload oder ein Feld für die URL zu einem Benutzerbild unter WordPress gibt.

Um neben dem Namen und der Beschreibung des Autoren auch ein Bild anzuzeigen, verknüpft Ihr in Euren Templates ein Bild einfach über den folgenden Code:

{% highlight html %}
<img src="<strong><?php bloginfo('template_directory'); ?></strong>/images/autor_id_<strong><?php the_author_ID(); ?></strong>.jpg" />
{% endhighlight %}

Der obige Code baut Euch die URL zu einem Bild zusammen. Angenommen Euer eigenes Profil hat die ID 4, dann ladet Ihr ein Bild mit dem Namen `autor_id_4.jpg` in das Image-Verzeichnis Eures aktiven Themes hoch. Den Link generiert WordPress automatisch mit Hilfe des Befehls `<?php bloginfo('template_directory'); ?>.`

Um dem Bild noch den Namen des Autoren mitzugeben, fügt Ihr am besten noch den folgenden Code ein:

{% highlight html %}
alt="Phlow-Autor <?php the_author() ?>
{% endhighlight %}


Zusätzlich steht Ihnen auch noch die Option unter WordPress zur Verfügung dem Profil einen Link auf eine Übersichtsseite mit sämtlichen Einträgen des jeweiligen Autors beizufügen:

{% highlight html %}
<?php the_author_posts_link(); ?>
{% endhighlight %}


## Code-Snippet für Autoreninfos unter WordPress-Beiträgen

{% highlight php startinline=true %}
<div id="autor-info">
    <a href="<?php the_author_url() ?>" title="Website von Autor <?php the_author() ?>"><img alt="Phlow-Autor <?php the_author() ?>" src="<?php bloginfo('template_directory'); ?>/images/images_user/autor_id_<?php the_author_ID(); ?>.jpg" /></a>
Dieser Artikel wurde am <?php the_time('d.F Y') ?> von <a title="Website von <?php the_author() ?>" href="<?php the_author_url() ?>"><strong><?php the_author() ?></strong></a> geschrieben.
<?php the_author_description() ?>
</div>
{% endhighlight %}

