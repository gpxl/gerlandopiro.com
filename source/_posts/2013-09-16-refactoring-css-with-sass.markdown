---
layout: post
title: "Refactoring CSS with Sass"
excerpt: "Finally digging deep"
date: 2013-09-16 14:10
published: true
external-url:
---
"Sass is an extension of CSS that adds power and elegance to the basic language. It allows you to use variables, nested rules, mixins, inline imports, and more, all with a fully CSS-compatible syntax. Sass helps keep large stylesheets well-organized, and get small stylesheets up and running quickly, particularly with the help of the Compass style library."

That text taken from the Sass reference page sums up what makes Sass awesome, it allows you to be more efficient with your CSS and removes a lot of the frustration that comes with the sprawling highly duplicated stylesheets that come with any reasonably sized project. 

I've been using Sass in my Rails apps for a few years now but I have yet to apply everything Sass has to offer in my own work. That has always been something that bugged me and so I'm finally going to do something about it.

With a couple of guide books in hand, The [Pragmatic Guide to Sass](http://pragprog.com/book/pg_sass/pragmatic-guide-to-sass) by Hampton and Michael Lintorn Catlin and [Scalable and Modular Architecture for CSS](http://smacss.com) by Jonathan Snook, I'm going to dig into Sass to see what techniques are most beneficial in refactoring and maintaining a medium sized site, Engineyard.com. 

The current [site CSS](https://www.engineyard.com/assets/application.css) weighs in at a hefty 162kb __after__ being compiled by the Rails Asset Pipeline and contains [__197 unique colors__ in __1488 css tags__](http://colorpalettes.gerlandopiro.com/colormaps/engineyard). Clearly there's a lot of work to be done, but it's going to be a lot of fun as well. 

### Follow along by joining my email list below.
