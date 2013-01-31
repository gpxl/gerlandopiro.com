---
layout: post
title: "The Minimalist Blogging Stack"
date: 2013-01-30 20:59
published: false
sharing: false
external-url:
---
As I alluded to in my initial $5 Web App Challenge post, I have not been a very active writer in the past. Over the years I've probably tried every blogging platform under the sun from hosted platforms like Blogger and Tumblr, to self hosted apps like Drupal and WordPress. Nothing ever seemed to click with me and I'd find myself spending my time yak shaving in hopes of progress. Inevitably I'd get frustrated and just give up, inspiration and motivation lost in the process. The solution, I found only recently, was to embrace constraints and simplify.

My current blogging stack consists of [IA Writer](http://www.iawriter.com) (editor), [Octopress](http://octopress.org) (blog), and S3 (hosting). It's a developer friendly set up so non-techies might have to learn some new tricks, but learning how to DIY never hurt anyone! Next I'll break down how each layer in the stack helps me work faster, run cheaper, and stay focused on writing.

## IA Writer

IA Writer is a wonderfully simple iOS and OSX text editor built for the sole purpose of distraction free writing. The application has practically no chrome and a few features, but the features that are extremely handy. First off is __focus mode__, a feature that allows you to focus on the current sentence by greying out all surrounding text. Files can be saved to iCloud so they are available when inspiration hits on any device with IA Writer installed. The iOS version adds special keys to ease navigating through documents by word or character. 

IA Writer also supports [Markdown formatted documents](http://daringfireball.net/projects/markdown/syntax#overview). This last feature is pretty awesome as Octopress also supports Markdown so you can easily cut and paste documents into an Octopress file or    _edit your Octopress files directly with IA Writer_. If you work that way you lose iCloud sharing across devices, but it's nice to have the option.

And finally, IA Writer has a preview window so you can see how your page will look before pushing it to your blog.

## Octopress

Keeping with the simple theme, Octopress is a blogging framework that turns the Wordpress model of content management on it's head. Instead of having managing content through a web application and pulling content form a database, Octopress generates a static version of your content on your local computer _before_ pushing to a web server. There are numerous benefits to this technique including much better security, faster response times, and much lower web server requirements.

Octopress posts are simple text files that can be edited in any text editor and automated tasks handle static file generation and web server deployment. 

Since the output of Octopress is static html and css, all you need is a web service that can handle static files, and that's where S3 comes in.

## Amazon S3

[Amazon S3](https://aws.amazon.com/s3), or Simple Storage Service, has an intentionally minimal feature set for storing and retrieving static content. It's very robust and extremely cost efficient with rates currently at $0.095/mo. for a GB of storage and $0.01 per 10,000 GET requests which means you can run a pretty well trafficked site for only pennies a month. The current version of Octopress does not come with support for deployments to S3 built in but it's [coming soon](https://github.com/imathis/octopress/pull/107). So you'll need to come up with your own method for syncing to S3 for now.

## Wrapping Up

My writing efforts are still in the nascent stage, but I'm really enjoying the technologies that have been chosen. I would love to hear what tools you use in your blogging efforts.
