---
layout: default
title: "Website Speed"
subtitle: "Optimierung von Websites"
---



## Optimierung der Bilder

Video-Tutorials von Phlow

## CSS: Zusammenfassen und Minifizierung
## Javascript: Zusammenfassen und Minifizierung
## Minifizierung von HTML
## GZIP Kompression
## Browser Caching aktivieren

Quelle Code für `.htaccess` <https://github.com/h5bp/html5-boilerplate/>.

~~~
<IfModule mod_expires.c>
  ExpiresActive on

# Perhaps better to whitelist expires rules? Perhaps.
  ExpiresDefault                          "access plus 1 month"

# cache.appcache needs re-requests in FF 3.6 (thx Remy ~Introducing HTML5)
  ExpiresByType text/cache-manifest       "access plus 0 seconds"

# your document html 
  ExpiresByType text/html                 "access plus 0 seconds"

# data
  ExpiresByType text/xml                  "access plus 0 seconds"
  ExpiresByType application/xml           "access plus 0 seconds"
  ExpiresByType application/json          "access plus 0 seconds"

# rss feed
  ExpiresByType application/rss+xml       "access plus 1 hour"

# favicon (cannot be renamed)
  ExpiresByType image/x-icon              "access plus 1 week" 

# media: images, video, audio
  ExpiresByType image/gif                 "access plus 1 month"
  ExpiresByType image/png                 "access plus 1 month"
  ExpiresByType image/jpg                 "access plus 1 month"
  ExpiresByType image/jpeg                "access plus 1 month"
  ExpiresByType video/ogg                 "access plus 1 month"
  ExpiresByType audio/ogg                 "access plus 1 month"
  ExpiresByType video/mp4                 "access plus 1 month"
  ExpiresByType video/webm                "access plus 1 month"

# htc files  (css3pie)
  ExpiresByType text/x-component          "access plus 1 month"

# webfonts
  ExpiresByType font/truetype             "access plus 1 month"
  ExpiresByType font/opentype             "access plus 1 month"
  ExpiresByType application/x-font-woff   "access plus 1 month"
  ExpiresByType image/svg+xml             "access plus 1 month"
  ExpiresByType application/vnd.ms-fontobject "access plus 1 month"

# css and javascript
  ExpiresByType text/css                  "access plus 2 months"
  ExpiresByType application/javascript    "access plus 2 months"
  ExpiresByType text/javascript           "access plus 2 months"

  <IfModule mod_headers.c>
    Header append Cache-Control "public"
  </IfModule>

</IfModule>
~~~

## Geschwindigkeit der Website testen


 * [PageSpeed Insights](http://developers.google.com/speed/pagespeed/insights/)
 * [Pingdom Website Speed Test](http://gtmetrix.com/)
 * [GTmetrix – Website Speed and Performance Optimization](http://tools.pingdom.com/fpt/)
 * []()
 * []()




 * [Caching Tutorial](https://www.mnot.net/cache_docs/)
 * [Leverage Browser Caching](http://www.feedthebot.com/pagespeed/leverage-browser-caching.html)
 * [How To Optimize Your Site With HTTP Caching](http://betterexplained.com/articles/how-to-optimize-your-site-with-http-caching/)
 * []()
 * []()
