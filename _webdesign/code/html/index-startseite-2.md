---
layout: page
subheadline: "HTML Code Snippets"
title: "Index Startseite Weiss"
teaser: ""
header:
    image: code_shutterstock_225068266.png
    background-color: "#900055"
    caption: »Flat design vector concept« von Shutterstock
    caption_url: http://www.shutterstock.com/pic.mhtml?id=225068266&src=id
# image:
#     thumb: icon/icon-html.svg
style: "#masthead-with-background-color { padding: 0; }"
categories:
    - code
tags:
    - html
    - code
---

<a href="{{ site.url }}/page/index-startseite-weiss.html">So sieht die Startseite aus ›</a>

{% highlight html %}
<!doctype html>
<html class="no-js" lang="de">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Startseite</title>

  <link href='http://fonts.googleapis.com/css?family=Roboto:900,300,700' rel='stylesheet' type='text/css'>

  <style type="text/css">
    body {
      background: #fff;
      color: #333;
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
      width: 800px;
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
      font-size: 3em;
      color: #333;
    }
  </style>
</head>
<body>
  <div class="wrapper">
    <h1>Hallo!</h1>
  </div>
</body>
</html>
{% endhighlight %}
