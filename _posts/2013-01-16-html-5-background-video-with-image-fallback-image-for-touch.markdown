---
author: mtyas-admin
comments: false
date: 2013-01-16 11:25:14+00:00
layout: post
link: http://matthewtyas.com/html-5-background-video-with-image-fallback-image-for-touch/
slug: html-5-background-video-with-image-fallback-image-for-touch
title: Background video with image fallback image for touch
wordpress_id: 788
categories:
- Blog
tags:
- CSS
- development
- HTML
- Jquery
- responsive
---

Quite a mouthfull but pretty much exactly what I googled when trying to solve this problem for a client recently.



_I will not in this article, be debating on whether having a full screen background video is a good or bad thing for users. I simply had a problem to solve._



## The problem





The client (the PR for a band) wanted their design overlaid on a full screen video (a twenty second b/w loop). The site also had to be responsive. In a meeting it was mentioned that the site needed to be built using HTML 5, "so the video will play on iPhone and iPad".





### Alarm bells





IOS touch devices (I am not sure on other devices at time of writing) will display a large play control in the centre of the video (in the case of this design therefore, right under the body copy) and if tapped the video will be played in the device's native player full screen thus rendering the site unusable. Therefore, clicking any link in the page is probably going to play the video and the user is going to be uncomfortably and unexpectedly shifted from the site to the video. Not even a useful video, a loop intended to give atmosphere to the design. Not to be viewed as a standalone piece of content.





## What to do?





Firstly I knocked up a quick test of what I explained above to show the client. I took their video, added position absolute to it and made it width and height 100%. Then I relatively positioned some content over the top. In a browser, not bad. On a mobile (my iPhone 5) the expected result. The client agreed this was not acceptable. Now, I could build a separate mobile site, as some people have ([whitelies.com](http://www.whitelies.com/) and [m.whitelies.com/](http://m.whitelies.com/)). but they did not want two sites to update, and I did not have budget to build two either.





## What now?





Okay, flash was out (for obvious reasons) and they were dead set on the video being present where possible. I could easily use media queries to set an image at small screen sizes and work mobile first to introduce the video at an appropriate breakpoint. That however, does not work well at all. For example my 11" Macbook Air is approximately the same size as a landscape iPad. I want the video on the Air but I want a fallback image on the Ipad…



_Given the length of the clip I even tried an animated gif, but at 20mb I was pushing it to say the least!_



After a bit of googling I realised I could use (Modernizr.touch) to at least serve an image based on whether the device was touch enabled instead.




    
    
    if (Modernizr.touch){
       // Show the image please
    } else {
       // Play the video, thank you Sir
    }
    





This still feels like sniffing really, and is not perfect by any means either. What will happen on a Microsoft surface…?





### After a bit more googling…





Finally I found the answer once I got on the Modernizr route and my searching took me too BigVideo.js which has a function using Modernizr touch to do exactly what I wanted ([http://dfcb.github.com/BigVideo.js/example-ambient-touch.html](http://dfcb.github.com/BigVideo.js/example-ambient-touch.html)). After [a bit of wrangling on Github](https://github.com/dfcb/BigVideo.js/issues/24) the demo was working and I was able to use the plugin to do exactly what I needed.





## The bigger picture





This has been an interesting problem that is not really solved. I believe under the circumstances I have used the best solution possible. If you have a better one, [please get in touch](http://matthewtyas.com/contact/).





The reason this is interesting is that the way we use devices is in a constant state of flux so the way manufacturers design them is also. In this case touch is not a good enough reason to not serve a video to a device. I am making assumptions about the devices usage.





I am having to assume that they are:






  * All 'mobile', and therefore may have slow connections or data usage limits


  * All have the same default behaviour with video as IOS touch devices





As mentioned above, this is not always true, touch screen desktops and laptop/tablet hybrids all exist. Some  are used both at home and away from home. Some may have default behaviour that limits our ability to do something and some don't. How can we as designers and developers provide as rich an experience as possible without knowing everything about a user, their device and environment, serving a fallback here and not there based on multiple users, devices and use cases?





## A line in the sand





The answer is we can't. We have to use our experience and knowledge, talk to our steak holders and users (if possible) and draw a line in the sand.
