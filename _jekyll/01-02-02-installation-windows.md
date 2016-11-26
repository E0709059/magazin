---
layout: page
title:  "Jekyll auf Windows-Rechnern installieren"
teaser: "Eine Schritt für Schritt-Anleitung, um den Website Generator Jekyll auf Windows-Rechnern zu installieren."
header:
    image: logo-jekyll.png
    background-color: "#333333"
image:
    thumb: icon/icon-jekyll.svg
chapter: "2.2"
permalink: /jekyll/installation-windows/
breadcrumb: true
---
<div class="alert-box radius warning" markdown="1">
Dieser Beitrag ist eine modifizierte Übersetzung von [»Learn how to run Jekyll, the blog-aware, static site generator in Ruby on Windows.«][8]. Die folgenden Schritte habe ich selbst nicht ausprobiert. Ich garantiere nicht dafür, dass diese Anleitung vollständig oder korrekt ist.
</div>

## Voraussetzungen für Jekyll

![Ruby Logo]({{ site.urlimg }}ruby-logo.png)

Um Jekyll auf einem Mac OS X-, Windows- oder Linux-Rechner zu installieren benötigt man die folgende freie Software:

* [Ruby](http://www.ruby-lang.org/en/downloads/)
* [RubyGems](http://rubygems.org/pages/download)


## #1 Ruby auf Windows installieren

![Windows Logo]({{ site.urlimg }}windows-mobile-logo.png)

Um Ruby auf Windows-Rechnern zu nutzen, muss man es zuerst installieren. Dafür eignet sich am Besten der Ruby Installer. Die aktuelle Version des Ruby Installers findet man unter [rubyinstaller.org][1].

Nach dem Download starten Sie einfach die `.exe`-Datei. Die Installation erledigt der Installer. Wichtig ist, dass man in der Checkbox »Add Ruby executables to your PATH« einen Haken setzt. Weitere Informationen findet man auf der offiziellen Ruby-Website unter [»Ruby installieren«][2].

## #2 Ruby DevKit installieren

Einige der so genannten *Dependencies* von Jekyll müssen nativ gebaut werden. Dazu ist das Ruby DevKit notwendig.

1. Laden Sie das Ruby DevKit-Paket unter [rubyinstaller.org][1] herunter.
	* Beachten Sie, dass Sie die richtige Versionsnummer des DevKits passend zu Ihrer Rechnerarchitektur herunterladen. Schauen Sie auf ihrem Rechner nach, ob Sie ein 32 Bit- oder 64 Bit-System nutzen.
2. Bevor Sie die Installation durchführen, beenden Sie am Besten alle anderen Programme. Führen Sie die `.exe`-Datei aus und wählen Sie als Ziel etwas wie `C:\rubydevkit\`.
3. Initialisieren Sie das DevKit und verknüpfen Sie mit der Ruby-Installation über Ihr bevorzugtes Kommandozeilenwerkzeug.
	* Navigieren Sie in den Ordner, in welchen Sie das DevKit extrahiert haben – z.B. `cd "C:\rubydevkit\"`.`
	* Geben Sie jetzt `ruby dk.rb init` ein, um automatisch Ruby-Installationen zu finden und fügen Sie diese Ihrer Konfigurationsdatei hinzu.
	* Installieren Sie das DevKit mit `ruby dk.rb install`.

## #3 Das Jekyll-Gem installieren

Installieren Sie die aktuelle Version von Jekyll über die Kommandozeile.

<div class="alert-box radius terminal" markdown="1">
$ gem install jekyll
</div>

Glückwunsch! Sie haben Ruby und Jekyll auf Ihrem Windows-System installiert.

<div class="alert-box radius success" markdown="1">
TIPP: Weitere Informationen zum Umgang mit Jekyll auf Windows-Rechnern findet man unter [»How to Run Jekyll on Windows«][8].
</div>



 [1]: http://rubyinstaller.org/downloads/
 [2]: https://www.ruby-lang.org/de/installation/
 [3]: https://developer.apple.com/xcode/downloads/
 [4]: https://itunes.apple.com/de/app/xcode/id497799835?mt=12
 [5]: http://support.apple.com/kb/HT2531?viewlocale=de_DE&locale=de_DE
 [6]: http://brew.sh/index_de.html
 [7]: http://www.damianthater.com/2013/02/09/2100-jekyll-blog-installation-ubuntu.html
 [8]: https://github.com/juthilo/run-jekyll-on-windows/
 [9]: #
 [10]: #