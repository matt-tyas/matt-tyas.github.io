---
author: mtyas-admin
comments: false
date: 2012-03-15 12:42:02+00:00
layout: post
link: http://matthewtyas.com/ie8-and-modenizr-bug/
slug: ie8-and-modenizr-bug
title: IE8 and Modernizr 2.5.2 links bug
wordpress_id: 457
categories:
- Blog
tags:
- CSS
- HTML
- IE
- Jquery
- modenizr
---

This week I've had an annoying and difficult to replicate bug with Modenizr 2.5.2 and Internet Explorer 8. 

Working for Leeds University IE8 is still our standard campus supported browser and during a dry run of a demo, links in our application were causing the browser to crash on page refresh. This behavior was only present in IE8 running in standards mode. The error we were getting was:


    
    res://ieframe.dll/acr_error.htm



Followed by the URL of the page we were trying to access. Off to Google we went and found similar cases over at github on respond.js and Modenizr issue threads. I decided to quickly take the background image of the site off the  tag and add a quick class of, 'background'. This fixed the issue on my VM.

As it turned out the clever Modenizr people had fixed the bug and an update of modenizr 2.5.2 to 2.5.3 should ensure we do not experience this problem again.

Needless to say the body class will remain until after our demo on Monday, just to be on the safe side.

Over and out.
