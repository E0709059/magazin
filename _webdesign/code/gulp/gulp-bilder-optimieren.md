---
layout: page
subheadline: Gulp.js
title: "Bilder optimieren mit Gulp"
teaser: "Bei der Bildkompression hilft Gulp und automatisiert die lästige, aber äußerst wichtige Bildkompression. Ob verlustlose Kompression oder verlustbehaftete Kompression: Für jedes Bildformat setzt Gulp auf die etablierten freien Bibliotheken zurück."
categories:
    - code
    - development
tags:
    - code
    - bildkompression
    - automatisierung
    - gulp
image:
    thumb: icon/icon-gulp-128x.png
---
Für die Optimierung von PNG-, JPG-, SVG- und GIF-Dateien stehen verschiedene freie Bibliotheken zur Verfügung. Dazu gehören [pngquant][1], [OptiPNG][2], [JpegOptim][3] oder [Scour][4].


{% highlight javascript %}
// 
// Gulp.js
// 
// 1. Create package.json › $ echo "{}" > package.json
// 2. Create gulpfile.js › $ touch gulpfile.js
// 3. Install Gulp-Plugins › $ npm install gulp gulp-changed gulp-rename gulp-image-resize gulp-imagemin --save-dev
// 

// gulp.js einbauen
var gulp = require('gulp'); 

// Plugins einbauen
var changed = require('gulp-changed'),
        rename = require('gulp-rename'),
        imageResize = require('gulp-image-resize'),
        imagemin = require ('gulp-imagemin');


// Pfade festlegen
var imgSrc = './originals/**/*',
        imgDst = './optimized/';


// Watch images files and resize and optimize
gulp.task('images', function() {
    console.log('\n---\n\n Watching Images, Optimizing Images \n\n---\n') 
    gulp.watch(imgSrc, ['thumb', 'imagemin']);
});

// Bilder und Vektoren minifizieren
gulp.task('imagemin', function() {
    gulp.src(imgSrc)
        .pipe(changed(imgDst))
        .pipe(imagemin())
        .pipe(gulp.dest(imgDst));
});

gulp.task('thumb', function () {
    gulp.src(imgSrc)
        .pipe(imageResize({ 
            width : 500,
            height : 281,
            crop : true,
            upscale : false,
            imageMagick: true
        }))
        .pipe(imagemin())
        .pipe(rename({suffix: '-thumb'}))
        .pipe(gulp.dest(imgDst));
});

gulp.task('large', function () {
    gulp.src(imgSrc)
        .pipe(imageResize({ 
            width : 1000,
            height : 700,
            crop : true,
            upscale : false,
            imageMagick: true
        }))
        .pipe(imagemin())
        .pipe(rename({suffix: '-large'}))
        .pipe(gulp.dest(imgDst));
});
{% endhighlight %}



## Anleitungen für die Optimierung von Bildern mit Gulp

* [Automating Image Optimization with Gulp](http://www.devworkflows.com/posts/adding-image-optimization-to-your-gulp-workflow/)


 [1]: http://pngquant.org/
 [2]: http://optipng.sourceforge.net/
 [3]: https://github.com/tjko/jpegoptim
 [4]: http://www.codedread.com/scour/
 [5]: #
 [6]: #
 [7]: #
 [8]: #
 [9]: #
 [10]: #