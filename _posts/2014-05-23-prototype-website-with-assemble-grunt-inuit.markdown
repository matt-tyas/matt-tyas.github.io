---
author: mtyas-admin
comments: false
date: 2014-05-23 10:26:02+00:00
layout: post
link: http://matthewtyas.com/prototype-website-with-assemble-grunt-inuit/
slug: prototype-website-with-assemble-grunt-inuit
title: Prototype Website with Assemble, Grunt & Inuit
wordpress_id: 1005
categories:
- Blog
tags:
- CSS
- Grunt
- HTML
- inuit.css
- SASS
---

Over the last year I have been moving away from GUI based tools in all of my work. Firstly to minimise spend on licenses but also to ensure I can move from machine to machine without effecting my workflow, whilst maintaining the speed of front end development I require.

To that end I have created a website prototyping framework using static site generator [Assemble.io](http://assemble.io/) and [inuit.css](https://github.com/csswizardry/inuit.css/) using [Grunt](http://gruntjs.com/) to output the static site using a series of tasks. This will allow me to quickly prototype or build static sites from anywhere as everything is of course, stored in GIT.

[Check out the prototype framework project here](https://github.com/matt-tyas/prototype-website).

_The Read me for ref is pasted here also._



## Prototype Framework



Front-end website prototype system, built with Assemble, Inuit.css and Grunt.



### Using this system



Install Node.js and Grunt.js

Then, once you have the project downloaded, run the command `npm install` in the root of the project.

Once this finishes running, you can build the project by running the command `grunt`

Credit where is is due. This is not a fork exactly, but an idea I got from [github.com/buildingblocks](https://github.com/buildingblocks). I have heavily simplified their very clever work to suit my own needs.



#### Assemble



Assemble is a component and static site generator that makes it dead simple to build modular sites, documentation and components from reusable templates and data.



#### Inuit.css



Powerful, scalable, Sass-based, BEM, OOCSS framework.



#### Grunt.js



In one word: automation. The less work you have to do when performing repetitive tasks like minification, compilation, unit testing, linting, etc, the easier your job becomes. After you've configured it, a task runner can do most of that mundane work for you—and your team—with basically zero effort.



### Documentation







  * To run the scss lint task you need to also install the scss gem `$ gem install scss-lint` [this article is helpful][9].


  * Run `$ scss-lint path/to/your/sass/files` on the scss to lint.


