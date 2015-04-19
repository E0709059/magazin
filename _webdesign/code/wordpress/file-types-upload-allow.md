---
layout: page
subheadline: "WordPress Rezepte"
title: "Weitere Dateitypen für den Upload erlauben"
teaser: "Mit der Methode <em>wp_check_filetype</em> verwaltet und erweitert man über die <em>functions.php</em> die Liste der zum Upload erlaubten Dateitypen. Um die Liste zu erweitern fügt man <code>'Dateiendung' => 'MIME-TYPE'</code> ein."
header:
    image: code_shutterstock_225068266.png
    background-color: "#900055"
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
breadcrumb: true
---

{% highlight php startinline=true %}
// Weitere Dateitypen für den Upload erlauben
//
// Mit der Methode *wp_check_filetype* verwaltet und erweitert man
// über die *functions.php* die Liste der zum Upload erlaubten Dateitypen
// Um die Liste zu erweitern fügt man 'Dateiendung' => 'MIME-TYPE' ein.
//
function get_allowed_mime_types() {
	static $mimes = false;
	if ( !$mimes ) {
		$mimes = apply_filters( 'upload_mimes', array(
			'jpg|jpeg|jpe' => 'image/jpeg',
			'gif' => 'image/gif',
			'png' => 'image/png',
			'bmp' => 'image/bmp',
			'tif|tiff' => 'image/tiff',
			'ico' => 'image/x-icon',
			'asf|asx|wax|wmv|wmx' => 'video/asf',
			'avi' => 'video/avi',
			// 'webm' => 'video/webm',
			// 'pdf' => 'application/pdf',
			// 'zip' => 'application/zip',
			// 'gz|gzip' => 'application/x-gzip',
		) );
	}                
{% endhighlight %}
