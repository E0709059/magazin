---
layout: video
subheadline: WordPress
title: Die Installation von WordPress
teaser: "Die Video-Anleitung »Die Installation von WordPress« erklärt, welche ersten Schritte für die Installation und Konfiguration der Weblog-Software notwendig sind."
header: no
image:
    thumb: phlow-tv-wordpress-installation-thumb.jpg
categories:
    - video
tags:
    - video
    - wordpress
    - installation
    - wordpress installation
iframe: "<iframe width='970' height='546' src='//www.youtube.com/embed/lW820hNkXrI' frameborder='0' allowfullscreen></iframe>"
permalink: /video/wordpress-installation/
video:
    embedURL: "https://www.youtube.com/embed/lW820hNkXrI"
    contentURL: "https://www.youtube.com/watch?v=lW820hNkXrI"
    thumbnailUrl: "http://img.youtube.com/vi/lW820hNkXrI/maxresdefault.jpg"
---
## Vorbereitung

Für Ihre eigene WordPress-Installation brauchen Sie:

1. Eigenen Webspace
2. Einen Server, der PHP unterstützt
3. Eine MySQL-Datenbank
4. Eine FTP-Programm, z.B. [FileZilla][1]
5. WordPress-Installationspaket



## Schritt 1: WordPress herunterladen und entpacken

Laden Sie das aktuelle WordPress-Installationspaket herunter und entpacken Sie die ZIP-Datei auf Ihrem Schreibtisch (Desktop).

* [Download Deutsche WordPress-Version](http://wpde.org/download/)
* [Download Englische WordPress-Version](http://wordpress.org/download/)



## Schritt 2: Erstellen Sie eine Datenbank bei Ihrem Webhoster

Damit WordPress auf Ihrem Webspace funktioniert, benötigen Sie eine Datenbank. Organisieren Sie sich von Ihrem Webhoster die folgenden Daten. Je nach Webhoster müssen Sie die Datenbank samt Passwort selbst anlegen.

* Datenbankname
* Datenbankbenutzername
* Datenbankpasswort



## Schritt 3: Laden Sie WordPress per FTP-Programm auf den Webspace hoch

Um das WordPress-Paket auf Ihren Webspace hochzuladen, brauchen Sie ein FTP-Programm. Die Videoanleitung [»Filezilla - Dateien hochladen per FTP-Programm«][9] erklärt Ihnen den Umgang mit dem kostenlosen FTP-Programm.

Um Ihr FTP-Programm mit dem Server verbinden, benötigen Sie die folgenden Daten von Ihrem Webhoster:

* Servername
* Benutzername für den Server
* Passwort für den Server



## Schritt 4: Installieren Sie WordPress

Nachdem alle WordPress-Dateien hochgeladen wurden, öffnen Sie WordPress unter der Internetadresse unter welcher Sie WordPress hochgeladen haben. Folgen Sie den Anweisungen Schritt für Schritt und geben Sie die gewünschten Daten ein.



## Schritt 5: Loggen Sie sich in WordPress ein

Nach der erfolgreichen Installation, können Sie sofort mit WordPress loslegen.



## Codeschnipsel: .htaccess Datei schützen

Mit diesem zusätzlichen Code-Schnipsel schützen Sie Ihre WordPress-Installation vor Übergriffen. Sie müssen es in die *.htaccess*-Datei einfügen.

~~~~
# Schützt die wp-config.php
<files wp-config.php>
Order deny,allow
deny from all
</files>
~~~~



{% include ad/das-wordpress-buch.html %}


## Verwendete Creative Commons Musik im Video

* [Comfort Fit][4] &middot; [&#8220;True Form&#8221; (MP3-Download)][6]
* [Dubmood][5] &middot; [&#8220;Kick de Bucket&#8221; (MP3-Download)][7]



 [1]: http://wpde.org/download
 [2]: http://wordpress.org/download/
 [3]: http://filezilla-project.org/
 [4]: http://www.comfortfit.de/
 [5]: http://www.dataairlines.net/dubmood/
 [6]: http://bit.ly/forget_remember_lp
 [7]: http://bit.ly/dubmood
 [8]: {{ site.url }}
 [9]: {{ site.url }}/video/filezilla/
