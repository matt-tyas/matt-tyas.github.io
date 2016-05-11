---
author: mtyas-admin
comments: false
date: 2012-10-17 20:05:36+00:00
layout: post
link: http://matthewtyas.com/keeping-pace-vs-web-guidelines/
slug: keeping-pace-vs-web-guidelines
title: Keeping Pace Vs Web Guidelines
wordpress_id: 500
categories:
- Blog
tags:
- day job
- design
- development
- guidelines
- HTML
- Leeds University
- responsive
---

_I recently wrote a justification for some design decisions I made whilst designing our team web site at work. The article below deals with bending web guidelines to allow the use of new techniques. I deal mainly with responsive design here but, I also touch upon the use of @font-face and icon fonts also. It was written primarily for an audience within marketing and management. It is where possible, none technical._



## Designing a Portfolio for the Web Team





### Our Requirements





The remit for the site was fairly simple. We needed it to do four things:







  * Explain in simple terms the way we work with clients to produce web sites and applications

	
  * Showcase our design and development work

	
  * Introduce users to our CMS system

	
  * Give the web team a fun and approachable feel





I put pencil to paper and quickly realised our requirements extended beyond the content and look and feel of the site. As the web team we have responsibility to stay up to date with recent trends and technologies. The web moves fast and so must we, or we are not doing our jobs properly.


					


### Why it is Beta





With this in mind I came up with a few extra requirements. Requirements that ultimately cause this site to be defined as Beta, within the context of the University.






	
  * What about mobile devices?

	
  * What about web fonts (@font-face)?

	
  * What about icon fonts?





### Guidelines for the Good





As with any large organisation we have guidelines for how we work with design for print and web. These guidelines are a good way for the University to keep consistent branding across all of its design work, whether produced internally or externally.





### Technology Moves Faster than our Guidelines





Technology changes, user behaviour changes, and it is important to adapt as quickly as possible to ensure the best possible experience for clients and customers. One example of this over the last five years has been the rise in mobile browsing. Browser manufacturers, developers and designers have seen the need for sites to adapt to better serve content to a bigger or smaller screen. I am not going to go in to how this works or when, when not, or to what degree it should be implemented. I will however say, that browsing on devices of different sizes and abilities (on a 3G network for example) is a different experience and, should be treated as such. Guidelines on the other hand are not rewritten quickly enough to reflect this changing landscape. They have to carefully crafted, agreed and communicated to the wider audience. This takes time, time that the web does not respect.





### My Way or the Guideline Way





I had to bend the guidelines. I decided to employ responsive techniques to make the content look as if it were designed specifically for whatever screen size you choose to view it on. In our case this was a standard desktop size of 960px down to a smart phone size of 320px. The content would shrink or stack based on a set of rules I would write in the code. As I started to design the navigation it became obvious I would have to bend the guidelines to fit the masthead in properly at all sizes. The current guidelines dictate the header of any University must appear as below, with navigation items under the page title and logo.




[![Current masthead](http://matthewtyas.com/wp-content/uploads/2012/05/masthead.png)](http://matthewtyas.com/wp-content/uploads/2012/05/masthead.png)
Masthead as featured in the current guidelines.




On a smaller screen the page title and the logo would begin to touch. I could drop the page title under the logo, but if the title was long, and with the format of the UoL logo, users on a small screen would loose a lot of space at the top of their browser. Add on some navigation under this banner and most if not all of the screen, is gone before any useful page content can be seen.




[![](http://matthewtyas.com/wp-content/uploads/2012/05/masthead-mobile.png)](http://matthewtyas.com/wp-content/uploads/2012/05/masthead-mobile.png)
Current masthead title and UoL logo begin to clash as smaller sizes, and we loose screen space. Add navigation as well and the issue gets worse.




### An Imperfect Solution





#### Desktop





I began by bending the guidelines and placed the navigation along side the logo aligned left within the masthead. I replaced the standard, 'Home', link with our name, 'Web Solutions' which fulfilled the need to identify who within the University we are whilst saving some screen space. While this works well for our site, it would not translate to a site with a large title. I was starting to find a solution for our site, but not the wider institution.




[![Web solutions desktop web site layout image](http://matthewtyas.com/wp-content/uploads/2012/05/desktop.png)](http://matthewtyas.com/wp-content/uploads/2012/05/desktop.png)
Web Solutions - desktop.

				


#### Tablet





As you approach tablet size the logo started the touch the navigation. I reformatted it into two columns of three links left aligned. This kept the navigation separated from the logo and thus retained the integrity of the design (resize the browser to see the effect).




[![Web solutions tablet size web site layout image](http://matthewtyas.com/wp-content/uploads/2012/05/tablet.png)](http://matthewtyas.com/wp-content/uploads/2012/05/tablet.png)
Web Solutions - tablet.




#### Mobile





As we get to mobile size the navigation is forced to drop under the logo, it still however stacks in two columns of three. The site title being part of the navigation however, helps to save real estate on the screen. The navigation items are now in rounded rectangles to define the button shape and they have a nice large area for fingers to press easily. The content slider below also has had its navigation changed from small dots to big left and right arrow buttons.




[![Web solutions mobile size web site layout image](http://matthewtyas.com/wp-content/uploads/2012/05/mobile.png)](http://matthewtyas.com/wp-content/uploads/2012/05/mobile.png)
Web Solutions - mobile.




### You keep saying you bent the Guidelines, you broke them?!





I am referring to having bent them as opposed to broke because I could have gone a lot further. For example the UoL logo. We had discussions in the office about the possibility of dropping the tower image off the logo at the smallest sizes. Leaving just the text portion, thus saving a lot of space in the top left of the screen. This was I believed a step too far however, without consulting the wider audience first.




[![Alternate Leeds University masthead layouts](http://matthewtyas.com/wp-content/uploads/2012/05/masthead-mobile-alt.png)](http://matthewtyas.com/wp-content/uploads/2012/05/masthead-mobile-alt.png)
Two examples of how the logo format may have to change at smaller sizes. No guidleines exist for small screens but these rough examples still break branding guidelines with regards to the logo, badly.

										


### Other Enhancements


					


#### Web Fonts


					


When the guidelines were written we lived in the era of the, 'web safe font'. There were only a handful of fonts you could safely use on a site to ensure your design was consistent for all users. Now due to font embedding and services such as [Typekit](https://typekit.com/) and [Font Deck](http://fontdeck.com/) we have a whole world of new fonts available to us. I opted to use Meta Serif for my headings to give the design a friendly feel, and Droid Sans (designed specifically for readability on screens at small sizes) for smaller text. These decisions may not fully fit in with the guidelines at present, but to create a solution that worked for us I felt they were decisions worth taking.


					


#### Icon Fonts


					


Icons are a useful tool for designers, as humans are visual an icon can help user understand the information in front of them a bit quicker and sometimes without the need of text at all. However with the introduction of retina (very high resolution) screens. Images and icons look fuzzy (on retina screens) or when zoomed in into. Using a web font that displays all your icons means they stay sharp at any size, on any screen and, reduce the size of the page as they do not require extra image files.


					


#### A Nod to Corporate


					


I may have bent or broken our old guidelines slightly to achieve a design that worked for our team's needs but at all times I had one eye on the corporate style. I think the site manages to push forward slightly what we at the University need to be doing with the web but also, stays true to the strong corporate style and branding.




[![Web solutions next to the corporate website image](http://matthewtyas.com/wp-content/uploads/2012/05/corporate.png)](http://matthewtyas.com/wp-content/uploads/2012/05/corporate.png)
I feel the Web Solutions site, sits well within the corporate family.




### In Conclusion





Nothing I have done here is perfect, nor is it meant to be. The techniques employed in this site are only a few years old at most, and in the context of the University are fairly cutting edge. I have not solved the masthead issue only performed an experiment that may yet feed into the solution for a responsive masthead that works across more than just one site. It is important that a personal or team site is seen in some respects as a playground and a showcase of what could happen in the future to keep us excited about our work and what we can do, to help the University push forward is digital strategy in the future.


					


Matt Tyas, Web Designer - ISS Web Solutions.
