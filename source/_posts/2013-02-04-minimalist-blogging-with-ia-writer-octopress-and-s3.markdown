---
layout: post
title: "Minimalist Blogging with IA Writer, Octopress and S3"
date: 2013-02-04 08:51
published: true
comments: true
external-url:
---
As I alluded to in my initial [$5 Web App Challenge](/2013/01/27/starting-the-5-dollars-web-app-challenge) post, I have not been an active writer in the past. In years past, I've probably tried every blogging platform under the sun from hosted platforms like Blogger and Tumblr, to self hosted apps like Drupal and WordPress. Nothing seemed to click and I'd find myself spending time [yak shaving](http://en.wiktionary.org/wiki/yak_shaving) instead of writing. Inevitably I'd get frustrated and give up; inspiration and motivation lost in the process. The solution, I found recently, was to embrace constraints and simplify.

My current "blogging stack" consists of IA Writer, Octopress, and Amazon S3. It's a developer friendly set up so non-techies might have to learn new tricks, but learning how to DIY is in itself very rewarding. In this post break down how each layer in the stack helps me work faster, run cheaper, and stay focused on writing.

### The Editor: IA Writer

The biggest improvement in my ability to write has been finding an editor that suited me well. [IA Writer](http://www.iawriter.com) is a wonderfully simple iOS and OSX text editor built for the sole purpose of distraction free writing. The application has practically no chrome and few features, but the features it _does_ have are extremely handy. First off is __focus mode__, this feature allows you to focus on the current sentence by greying out all surrounding text. Files can be saved to iCloud you can write and edit on either iOS or OSX whenever inspiration hits. The iOS version adds special keys to ease navigating through documents by word or character. 

Most important in my mind is that IA Writer supports [Markdown formatted documents](http://daringfireball.net/projects/markdown/syntax#overview). This last feature is pretty awesome as the blog software I use, Octopress, also supports Markdown. This shared feature means you can easily cut and paste documents into an Octopress file or _edit your Octopress files directly with IA Writer_. IA Writer has a preview window so you can be sure your Markdown renders as you expect it to.

### The Blog: Octopress

In keeping with the theme of simplicity, I prefer [Octopress](http://octopress.org) as my blogging platform. Most blog platforms, such as Wordpress, are delivered as web applications. In contrast, Octopress is a static file compiler that generates your entire site on your local computer _before_ pushing to a web server. Octopress does not require a web application to deliver or manage content and as such, benefits from better security, faster response times, and much lower web server requirements.

Octopress posts are simple text files that can be formatted with Markdown syntax and can be edited in any text editor. Site generation and web server deployment are managed through scripted Rake tasks.

Since the output of Octopress is static html and css, all you need is a web service that can handle static files, and that's where Amazon S3 comes in.

### The Web Host: Amazon S3

[Amazon S3](https://aws.amazon.com/s3) has an intentionally minimal feature set for storing and retrieving static content. It's very robust and extremely cost efficient with rates currently at $0.095/mo. for a GB of storage and $0.01 per 10,000 GET requests which means you can run a pretty well trafficked site for only pennies a month. Amazon consistently improves service and prices in their efforts to dominate market share, so  S3's value over time will only increase.

Octopress does not currently support deployments to S3 by default, but it's [coming soon](https://github.com/imathis/octopress/pull/107) and there are some [good articles](http://www.jerome-bernard.com/blog/2011/08/20/quick-tip-for-easily-deploying-octopress-blog-on-amazon-cloudfront) on how to DIY it for the impatient.

### Wrapping Up

My writing efforts are still in the nascent stage, but I'm confident I have finally have a set of tools that match my preferred way of working. Embracing constraints and using a few simple tools has allowed me to focus on the task of writing and to publish on a reliable, robust web host for pennies a month.
