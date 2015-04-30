---
layout: page
subheadline: "PHP Rezepte"
title: "Dateien innerhalb eines Verzeichnisses ausgeben"
teaser: ""
header:
    image: code_shutterstock_225068266.png
    background-color: "#900055"
    caption: »Flat design vector concept« von Shutterstock
    caption_url: http://www.shutterstock.com/pic.mhtml?id=225068266&src=id
image:
    thumb: icon/icon-php.svg
style: "#masthead-with-background-color { padding: 0; }"
categories:
    - code
tags:
    - php
    - rezept
    - code
---

{% highlight php startinline=true %}
<!doctype html>
<html class="no-js" lang="de">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Index</title>

<style type="text/css">
body,html {
  margin: 0;
  padding: 0;
  font-family: 'Neue Helvetica', Arial, sans-serif;
}
a {
  color: #0085ba;
  text-decoration: none;
}
a:hover {
  text-decoration: underline;
}
nav {
  background: #4b4b4d;
  padding: 8px 0 0 30px;
  margin: 0 0 30px 0;
  height: 42px;
  width: 100%;
}
#logo {
  display:block;
  width:            87px;
  height:           31px;
  background-image: url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAFcAAAAfCAYAAACSw1FtAAAAGXRFWHRTb2Z0d2FyZQBBZG9iZSBJbWFnZVJlYWR5ccllPAAAAyJpVFh0WE1MOmNvbS5hZG9iZS54bXAAAAAAADw/eHBhY2tldCBiZWdpbj0i77u/IiBpZD0iVzVNME1wQ2VoaUh6cmVTek5UY3prYzlkIj8+IDx4OnhtcG1ldGEgeG1sbnM6eD0iYWRvYmU6bnM6bWV0YS8iIHg6eG1wdGs9IkFkb2JlIFhNUCBDb3JlIDUuMC1jMDYwIDYxLjEzNDc3NywgMjAxMC8wMi8xMi0xNzozMjowMCAgICAgICAgIj4gPHJkZjpSREYgeG1sbnM6cmRmPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5LzAyLzIyLXJkZi1zeW50YXgtbnMjIj4gPHJkZjpEZXNjcmlwdGlvbiByZGY6YWJvdXQ9IiIgeG1sbnM6eG1wPSJodHRwOi8vbnMuYWRvYmUuY29tL3hhcC8xLjAvIiB4bWxuczp4bXBNTT0iaHR0cDovL25zLmFkb2JlLmNvbS94YXAvMS4wL21tLyIgeG1sbnM6c3RSZWY9Imh0dHA6Ly9ucy5hZG9iZS5jb20veGFwLzEuMC9zVHlwZS9SZXNvdXJjZVJlZiMiIHhtcDpDcmVhdG9yVG9vbD0iQWRvYmUgUGhvdG9zaG9wIENTNSBNYWNpbnRvc2giIHhtcE1NOkluc3RhbmNlSUQ9InhtcC5paWQ6NkUyMjY4NTQ3MkUyMTFFMkI4NUE4NDU0OUY5MTM4MUYiIHhtcE1NOkRvY3VtZW50SUQ9InhtcC5kaWQ6NkUyMjY4NTU3MkUyMTFFMkI4NUE4NDU0OUY5MTM4MUYiPiA8eG1wTU06RGVyaXZlZEZyb20gc3RSZWY6aW5zdGFuY2VJRD0ieG1wLmlpZDo2RTIyNjg1MjcyRTIxMUUyQjg1QTg0NTQ5RjkxMzgxRiIgc3RSZWY6ZG9jdW1lbnRJRD0ieG1wLmRpZDo2RTIyNjg1MzcyRTIxMUUyQjg1QTg0NTQ5RjkxMzgxRiIvPiA8L3JkZjpEZXNjcmlwdGlvbj4gPC9yZGY6UkRGPiA8L3g6eG1wbWV0YT4gPD94cGFja2V0IGVuZD0iciI/PvWvLQMAAAjRSURBVHja5FoLlE5V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');
}
h2 {
  font-weight: normal;
  font-size: 2.5em;
  margin: 10px 0 10px 0;
}
#wrapper {
  padding: 0px 30px;
}
ul {
  margin: 0;
  padding: 0 0 0 20px;
}
li {
  line-height: 1.5em;
}
footer {
  height: 180px;
}

</style>
</head>
<body>
  <nav>
    <a id="logo" class="top" href="http://phlow.de/"></a>
  </nav>

  <div id="wrapper">

<?php

// Bau die URL zur Datei auf
// http://stackoverflow.com/questions/3429262/get-base-directory-of-current-script

$url = $_SERVER['REQUEST_URI']; //returns the current URL
$parts = explode('/',$url);
$directory = $_SERVER['SERVER_NAME'];
for ($i = 0; $i < count($parts) - 1; $i++) {
 $directory .= $parts[$i] . "/";
}

// zeigt alle Dateien und Ordner an.
$dir = @opendir("."); //aktuelles Verzeichnis öffnen
$array = array();
$array_dirs = array();

 while( $file = @readdir($dir) )
 {

   //Filtert jetzt auch alle .htaccess und index.php
   if( $file != '.' && $file != '..' && $file !=".htaccess" && $file !="index.php" && $file !="x.php" )
   {
     if( is_dir($file) ) {
        array_push($array_dirs, $file);
     } else {
        array_push($array, $file);
     }
  }
 }

@closedir($dir);
natcasesort($array);
natcasesort($array_dirs);

?>
    <h2>Data</h2>

    <ul>
<?php // gibt alle Files aus 

      while($file = array_shift($array) ) {

       echo '      <li><a href=' .$file. '>'. $directory . $file.'</a></li>'. "\xA";

      } ?>
    </ul>


  </div><!-- /#wrapper -->

  <footer>
    <p><small>&copy; by Phlow Media 2000-<?php echo date('Y'); ?></small></p>
  </footer>
</body>
</html>
{% endhighlight %}
