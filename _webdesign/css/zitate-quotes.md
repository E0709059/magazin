---
layout: default
icon: css-logo.png
title: "Zitate"
description: ""
tags:
	- css
---
Schöne Zitate auf 

http://www.usertesting.com/blog/2014/08/06/choosing-the-right-font-a-guide-to-typography-and-user-experience/


#content  .entry-content .UTCallout{
    font-family: museo-slab,serif;
    font-size:32px;
    line-height: 36px;
    font-weight: normal;
    color: #68b246;
    padding: 45px ;
    margin: 40px 0;
    background:#F2F2F2;
    position:relative;
    z-index:1;
    font-style: italic;
    overflow: hidden;
}

#content  .entry-content .UTCallout:before{
display: block;
content: "\201C";
font-size: 325px;
left: -20px;
top: 100px;
color: #fff;    
font-family: Georgia, serif;
position: absolute;
z-index: -1;
font-style: normal;
font-weight: 100;
}

#content  .entry-content .UTCallout:after{  
font-style: normal;
display: block;
content: "\201D";
font-size: 325px;
right: -15px;
bottom: -70px;
color: #fff;    
font-family: Georgia, serif;
position: absolute;
z-index: -1;

}


