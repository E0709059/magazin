---
layout: page
subheadline: "HTML Code Snippets"
title: "Index Startseite für Phlow"
teaser: ""
header:
    image: code_shutterstock_225068266.png
    background-color: "#900055"
    caption: »Flat design vector concept« von Shutterstock
    caption_url: http://www.shutterstock.com/pic.mhtml?id=225068266&src=id
image:
    thumb: icon/icon-html-128x.png
style: "#masthead-with-background-color { padding: 0; }"
categories:
    - code
tags:
    - html
    - code
breadcrumb: true
---

<a href="{{ site.url }}/page/index.html">So sieht die Startseite aus ›</a>

~~~
<!doctype html>
<html class="no-js" lang="de">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Phlow</title>

<link href='http://fonts.googleapis.com/css?family=Roboto:900,300,700' rel='stylesheet' type='text/css'>

  <style type="text/css">
body {
  background: #222;
color: #fabb00;
text-shadow: rgba(0, 0, 0, 0.498039) 0px 1px 3px;
}
a {
  text-decoration: none;
  border-bottom: 1px dotted #4b4b4d;
color: #aa0132;
}
a:hover {
  border-bottom: 3px solid #aa0132;

}
.wrapper {
  margin: 0 auto;
  width: 620px;
font-weight: 300;
font-family: Roboto, 'Neue Helvetica', Helvetica, Arial;
}
dt { font-weight: 700; font-size: 1.5em; padding-bottom: 10px; }
dd { margin: 0 0 20px 0;}
ul {
  margin: 0;
  padding: 0;
  list-style: none;
}
li {
  display: inline;
}
h1 { 
  margin: 100px 0 0 0;
font-weight: 900;
font-family: Roboto, 'Neue Helvetica', Helvetica, Arial;
font-size: 14em;
color: #fabb00;


  text-shadow: -10px 10px 0px #aa0132,
                 -20px 20px 0px #771e1e,
                 -30px 30px 0px #4b4b4d;
}
  </style>
</head>
<body>
<div class="wrapper">
  <h1>Phlow</h1>
  <ul>
    <li>
    <a href="http://www.youtube.com/PhlowMedia" target="_blank" id="social-youtube" title="Videos, Video-Anleitungen und Filme von Phlow auf YouTube">YouTube</a>&nbsp;&nbsp;&middot;&nbsp;</li>
    <li>
    <a href="http://twitter.com/phlow" target="_blank" id="social-twitter" title="Immer das Neuste von Phlow gibt es auf Twitter">Twitter</a>&nbsp;&nbsp;&middot;&nbsp;</li>
    <li>
    <a href="http://www.facebook.com/phlow.media" target="_blank" id="social-facebook" title="Lass uns Freunde sein!">Facebook</a>&nbsp;&nbsp;&middot;&nbsp;</li>
    <li>
    <a href="http://soundcloud.com/phlow" target="_blank" id="social-soundcloud" title="Sounds und Downloads und mehr">Soundcloud</a>&nbsp;&nbsp;&middot;&nbsp;</li>
    <li>
    <a href="http://github.com/phlow" target="_blank" id="social-github" title="Code und mehr...">GitHub</a>&nbsp;&nbsp;&middot;&nbsp;</li>
    <li>
    <a href="http://instagram.com/phlowmedia" target="_blank" id="social-instagram" title="Bilder und Impressionen mit und ohne Filter...">Instagram</a>&nbsp;&nbsp;&middot;&nbsp;</li>
    <li>
    <a href="http://www.mixcloud.com/phlow/" target="_blank" id="social-mixcloud" title="Mixe, was sonst?">Mixcloud</a></li>
    </ul>
</div>

</body>
</html>
~~~
