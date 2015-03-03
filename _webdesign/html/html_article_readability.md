---
layout: default
isSubmenu: true
menutitle: ""
icon: html-logo.png
title:  "Readability Artikel-Vorlage"
subtitle: ""
date: 
description: "Diese Vorlage basiert auf der Vorgabe des Microformats von Readability"
tags:
  - html
---
Diese Vorlage basiert auf der Vorgabe des [Microformats von Readability][1] Mehr zu diesen »Article Publishing Guidelines« [liest man auf der Website][1].

<pre><code class="lang-html">

<article class="hentry">
  <header>
    <h1 class="entry-title"></h1>
    <h2 class="entry-summary"></h2>
    <time class="published" datetime="2012-01-07 11:11:03-0400">
      01-07-2012
    </time>
    <p class="byline author vcard">
        Von <span class="fn"></span>
    </p>
  </header>
  <div class="entry-content">
      <p>Text</p>
      <p>Text</p>
      <figure>
        <img src="tammy-strobel.jpg" alt="Portrait of Tammy Strobel" />
        <figcaption>Bildunterschrift</figcaption>
      </figure>
        <p>Text</p>

          <aside>
            <h2>Share this Article</h2>
            <ul>
              <li>Facebook</li>
              <li>Twitter</li>
              <li>Etc</li>
            </ul>
          </aside>
 
          <div class="entry-content-asset">
            <a href="photo-full.png">
              <img src="photo.png" alt="The objects Tammy removed from her life" />
            </a>
          </div>
 
          <a class="entry-unrelated" href="http://fake.site/">Find Great Vacations</a>
      </div>
 
      <footer>
        <p>Text</p>
        <div class="source-org vcard copyright">
            Copyright 2013 <span class="org fn">Phlow Media</span>
        </div>
      </footer>
    </article>

</code></pre>





 [1]: https://www.readability.com/developers/guidelines