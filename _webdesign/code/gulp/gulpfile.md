---
published: false
layout: page
subheadline: Gulp.js
title: "gulpfile.js für die Webentwicklung von Phlow Magazin"
teaser: ""
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
<pre>
// 
// Gulp.js
// 
// 1. Create package.json › $ echo "{}" > package.json
// 2. Install Gulp and Plugins › $ npm install gulp gulp-changed gulp-concat gulp-uglify gulp-rename gulp-imagemin gulp-minify-css --save-dev
// 
// 

// gulp.js einbauen
var gulp = require('gulp'); 


// Plugins einbauen
var changed = require('gulp-changed'),
    concat = require ('gulp-concat'),
    uglify = require ('gulp-uglify'),
    rename = require('gulp-rename'),
    imagemin = require ('gulp-imagemin'),
    imageResize = require('gulp-image-resize'),
    minifyCSS = require ('gulp-minify-css');


// Pfade festlegen
var outputDir = './jekyll-feeling-responsive/assets',
    javascriptSrc = [
                    './foundation/bower_components/jquery/dist/jquery.min.js',
                    './foundation/bower_components/foundation/js/foundation.min.js',
                    './foundation/js/jquery.backstretch.js',
                    './foundation/js/app.js'
                    ],
    stylesSrc = './foundation/stylesheets/**/*.css',
    modernizrSrc = './foundation/bower_components/modernizr/modernizr.js';



gulp.task('watch', function() {
  // Watch .css files
  console.log('\n- - - - - - - - - - - - - - - \n   Watch out, Gulp started!\n- - - - - - - - - - - - - - - \n')
  gulp.watch(stylesSrc, ['css']);
  gulp.watch(javascriptSrc, ['js']);
});



// CSS
gulp.task('css', function() {
    gulp.src(stylesSrc)
        .pipe(gulp.dest(outputDir + '/css'))
        .pipe(minifyCSS())
        .pipe(rename({suffix: '.min'}))
        .pipe(gulp.dest(outputDir + '/css'))
});


// Javascript Reduziert
var jsminSrc = [
    './foundation/bower_components/foundation/js/vendor/jquery.js',
    './foundation/bower_components/foundation/js/vendor/fastclick.js',
    './foundation/bower_components/foundation/js/foundation/foundation.js',
    './foundation/bower_components/foundation/js/foundation/foundation.accordion.js',
    './foundation/bower_components/foundation/js/foundation/foundation.clearing.js',
    './foundation/bower_components/foundation/js/foundation/foundation.dropdown.js',
    './foundation/bower_components/foundation/js/foundation/foundation.equalizer.js',
    './foundation/bower_components/foundation/js/foundation/foundation.magellan.js',
    './foundation/bower_components/foundation/js/foundation/foundation.topbar.js',
    './foundation/js/jquery.backstretch.js',
    './foundation/js/app.js'
    ];

gulp.task('js', function() {
    gulp.src(jsminSrc)
        .pipe(concat('javascript.js'))
        .pipe(gulp.dest(outputDir + '/js'))
        .pipe(uglify())
        .pipe(rename({suffix: '.min'}))
        .pipe(gulp.dest(outputDir + '/js'));
});


// Minifiziere Modernizr
gulp.task('modernizr', function() {
    gulp.src(modernizrSrc)
        .pipe(gulp.dest(outputDir + '/js'))
        .pipe(uglify())
        .pipe(rename({suffix: '.min'}))
        .pipe(gulp.dest(outputDir + '/js'))
});



// Jekyll samt Server starten
gulp.task('default', ['watch','js','css'], function () {
    require('child_process').spawn('jekyll', ['serve', '--config', '_config.yml,_config_dev.yml'], {stdio: 'inherit', cwd: 'jekyll-feeling-responsive'});
    require('child_process').spawn('bundle', ['exec', 'compass', 'watch'], {stdio: 'inherit', cwd: 'foundation'});
});

</pre>