---
author: mtyas-admin
comments: false
date: 2014-04-24 14:44:46+00:00
layout: post
link: http://matthewtyas.com/zurb-ink-and-mail-chimp-responsive-email-integration/
slug: zurb-ink-and-mail-chimp-responsive-email-integration
title: Zurb Ink and Mail Chimp Responsive Email Integration
wordpress_id: 980
categories:
- Blog
tags:
- day job
- development
- email
- HTML
- responsive
---

I only seem to blog about obscure little problems that make me want to tear my own eyes out, mainly because these are the problems I wish I had an answer to the most. In this case maybe I did something silly I have not noticed, or maybe I found a work around to a bug. Either way, if you end up here and you are experiencing this problem I hope this helps you save a bit of time.



## Zurb Ink



A project recently landed on my desk that seemed like the perfect candidate to try out Zurb's [Ink](http://http://zurb.com/ink/). An excellent, well researched framework you can use to create bullet proof HTML emails. After coding up the design using Ink. Bam! I had a responsive email that was displaying in all the major, browser based, native mobile and even Outlook (yes, all the Outlook) clients.

I was so 'appy I done a tweet I did:



<blockquote>Hot damn, responsive email passing all tests in Litmus on the first test. God bless you [@ZURBink](https://twitter.com/ZURBink)
> 
> -- matthew tyas (@MattTyas) [April 16, 2014](https://twitter.com/MattTyas/statuses/456438228925808640)</blockquote>






## Mail Chimp Integration



I'm a big fan of how easy Mail Chimp is to use. _It is very easy to use_ and I've been using it regularly and recommending it for a good few years now. This was however going to be the first responsive email template I'd created in the system, but since the code had been tested as a static mailer I was confident, it would be mostly a cut and paste job.



### The Problem



I started to define my editable areas using:


    
    
    mc:edit="i-wanna-edit-this-image-yo"
    



Nice and simple, however when I tested the email, any images that had a natural size over the wrapper of the email (which could be anything from 600px and smaller) no longer scaled and were retaining their natural width, thus breaking my lovely responsive layout...



### Before Editable Areas



![email working](http://matthewtyas.com/wp-content/uploads/2014/04/tbp-email-nice.jpg)



### After



![email broken](http://matthewtyas.com/wp-content/uploads/2014/04/tbp-email-busted.jpg)



## What the..?!



The images show Mail Chimp's preview mode, but this view was holding true in tests too. Bugger - all I had done was define the image as editable. Nothing else had changed in the mark-up or the CSS. 

Inspecting the code showed nothing (and I really mean nothing) that I could find that was adding this width. I Googled around and found [this thread on the Ink forum](http://foundation.zurb.com/forum/posts/4344-ink-through-mailchimp-is-not-responsive-on-iphone) that gave the advice to remove the standard mail Chimp footer, which I did. This, in my case had no effect. I tried it even though I had observed that deleting this image node from the DOM fixed the issue anyway.

In the end I found that it was Ink's own CSS:


    
    
    @media only screen and (max-width: 600px) {
      table[class="body"] img {
        width: auto !important; height: auto !important;
      }
    }
    



That was causing the problem. Why you ask? As the code had already proven to be working in tests? At this stage I honestly don't know. I would love to find out though. Please [get in touch](http://matthewtyas.com/contact/) if you get to the bottom of this!



## Solution



In the end I simply added a custom rule to the CSS to override the Ink code where ever I needed it as my post on the Ink forum explains:

_Okay. To any other lost souls who end up here, here's how I fixed the issue._

_Ink applies:_


    
    
    @media only screen and (max-width: 600px) {
      /* to give a sensible auto width under 600px */
      table[class="body"] img {
        width: auto !important; height: auto !important;
      }
    }
    



_For some reason (that I never quite got to the bottom of) as soon as you define an image as editable Mail Chimp forces these images to retain their original width, breaking your lovely Ink layout._

_In the end, in my custom styles I simply added:_


    
    
    @media only screen and (max-width: 600px) {
    /* I apply the .responsive-image class to any wrapping table where I want 100% rather than auto */
    table.body table.responsive-image img {
        width: 100% !important; height: auto !important;
      }
    }
    



_And everything was okay. I do not know why this was happening really which is worrying, but my template is now performing as expected._

So there you have it, and now the template is working - but what did I miss that Mail Chimp is adding after an image is defined as editable that makes Ink go so crazy?

Right now, I'm not sure.
