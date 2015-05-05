---
layout: page
title:  "Jekyll installieren"
teaser: "Eine Schritt für Schritt-Anleitung, um den Website Generator Jekyll auf dem eigenen Rechner zu installieren."
chapter: "2"
permalink: /jekyll/installation/
---
## Voraussetzungen für Jekyll

![Ruby Logo]({{ site.urlimg }}ruby-logo.png)

Um Jekyll auf einem Mac OS X-, Windows- oder Linux-Rechner zu installieren benötigt man die folgende freie Software:

* [Ruby](http://www.ruby-lang.org/en/downloads/)
* [RubyGems](http://rubygems.org/pages/download)

### Jekyll auf Linux installieren

![Linux Logo]({{ site.urlimg }}linux-logo-512x594.png)

Da ich nicht mit Linux vertraut bin, übergehe ich an dieser Stelle die Installation von Jekyll auf Linux-Systemen und verweise auf einen Artikel von Damian Thater: [»Jekyll auf Ubuntu installieren«][7].

### Jekyll auf Windows installieren

![Windows Logo]({{ site.urlimg }}windows-mobile-logo.png)
Die Installation von Ruby und Jekyll ist auf Windows-Rechnern ein wenig komplexer als die Installation auf Linux- oder OS X-Rechnern. Die Installationsanweisungen finden Sie in meinem Artikel [»Jekyll auf einem Windows-Rechner installieren«][10]. 


## Jekyll auf Mac OS X installieren

### #1 Ruby auf Mac OS X installieren und aktualisieren

#### XCode installieren

![Mac OS X Mavericks Logo]({{ site.urlimg }}icon-xcode.png)

Ruby ist auf Mac OS X-Rechnern bereits installiert. Um jedoch einwandfrei mit Jekyll und Ruby zu arbeiten, installiert man am Besten das von Apple zur Verfügung gestellte kostenlose [XCode][3]-Paket mit zahlreichen Entwicklerwerkzeugen. Für Jekyll brauchen Sie das Kommandozeilenwerkzeug, das Terminal.

Xcode kann man auch über den [App Store herunterladen][4].

#### Terminal starten

Starten Sie jetzt das Terminal. Dieses finden Sie entweder über den Finder unter Programme oder Sie öffnen es über [Spotlight][5]. Ich kann Ihnen nur die Tastenkombination <kbd>CMD</kbd> + <kbd>Leertaste</kbd> empfehlen. Anschließend tippen Sie sofort weiter `terminal` in die Suchmaske ein.

In der Regel reichen aber bereits die ersten drei Buchstaben. Bestätigen Sie anschließend mit der Eingabetaste die Auswahl im Ausklappmenü. Das ist auch in Zukunft der schnellste Weg Jekyll zu starten.

Um das gesamte System zu aktualisieren und es auf den aktuellen Stand zu bringen, tippen Sie als nächstes den folgenden Befehl ins Terminal.

<div class="alert-box radius terminal" markdown="1">
$ sudo gem update --system
</div>

#### Ruby mit Homebrew (OS X) installieren

Viele Anwender verwenden unter OS X [Homebrew][6] als Paketverwaltung. Ruby wird damit folgendermaßen installiert:


<div class="alert-box radius terminal" markdown="1">
$ brew install ruby
</div>




## #2 Jekyll-Gem installieren

<div class="alert-box radius terminal" markdown="1">
$ gem install jekyll  
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
 [10]: {{ site.url }}/anleitung/jekyll-windows-installation/