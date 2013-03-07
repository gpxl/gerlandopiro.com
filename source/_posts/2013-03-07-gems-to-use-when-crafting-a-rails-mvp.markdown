---
layout: post
title: "Gems to use when crafting a Rails MVP"
excerpt: "A handy list of my go-to gems."
date: 2013-03-07 09:19
published: true
external-url:
---

When creating a new web application there's some basic functionality that you will probably want to add and get out of the way so you can start building out your core business logic. A lot of that functionality can be found pre-baked in the RubyGems ecosystem but the overwhelming number of gems, 52k and counting, makes it hard to know what to use and what's crap. Here's a list of useful gems to get your app bootstrapped so the real work can begin.

## Authentication

Almost every web application needs user authentication and authorization capabilities. The gems below make it easy.

__[Devise](http://rubygems.org/gems/devise)__: Devise is a flexible authentication solution that makes it easy to add user registration and login capabilities to your app. Devise has built-in Omniauth support so you can quickly integrate with 3rd parties such as [Twitter](https://github.com/arunagw/omniauth-twitter), [Facebook](https://github.com/mkdynamic/omniauth-facebook), and just about [everyone else](https://github.com/intridea/omniauth/wiki/List-of-Strategies).

__[CanCan](http://rubygems.org/gems/cancan)__: CanCan is an authorization solution that works well with Devise and makes implementing access roles easy. All roles are defined in an Ability class that works with your User attributes to allow/deny access to your controller actions. 


## Upload management

If your users want to contribute assets, let them!

__[Paperclip](http://rubygems.org/gems/paperclip)__: Paperclip makes adding files to models relatively simple. You can configure image files for post-processing with Imagemagick. And out of the box Paperclip supports local file, S3, and fog storage with Azure and Dropbox available as add-on gems.   

_(alternative)_ ___CarrierWave__: I have not used CarrierWave yet since Paperclip gets the job done. I've heard some say they prefer it over Paperclip so it's worth checking out if Paperclip doesn't float your boat.

## Payment Processing

What's the point in having customers if you can't bill them?

__[Stripe](http://rubygems.org/gems/stripe)__: [Stripe](https://stripe.com/) refers to itself as themselves as "Payments for developers" and so it's fitting that they have an excellent api and robust tools to make it easy to integrate. You can also allow your customers to take payments through your site, although they need to have a Stripe account as well. 

_(alternative)_ ___[Active Merchant](http://rubygems.org/gems/activemerchant)__: If you want to support multiple payment processors Active Merchant is the way to go. It provides an abstraction layer that supports a ridiculous amount of [gateways](https://github.com/Shopify/active_merchant/wiki/gatewayfeaturematrix). Active Merchant was a direct extraction from [Shopify](http://www.shopify.com) so it's been 'battle-tested'.

## Frontend

These make life easier for developers writing the view layer, and for users submitting text content.

__[Haml](http://rubygems.org/gems/haml)__: [Haml](http://haml.info) is an alternative syntax for html that, in my opinion, is WAY better to work with than plain HTML. Unlike HTML it's whitespace sensitive and does not require closing tags. This does a good job of enforcing proper formatting habits and removes the mental overhead of closing tags in your more heavily nested pieces of layout.

I've interacted with some that absolutely hate Haml so it's certainly a  personal preference, but I would suggest you give it a chance.

__[github-markdown](http://rubygems.org/gems/github-markdown)__: Markdown is a lightweight syntax that makes writing and formatting text easy. Github's variant adds a few changes to traditional [Markdown](http://daringfireball.net/projects/markdown) syntax and, since they use it extensively on Github.com, it should be well supported for the foreseeable future.  

## SEO

The grey area of the web...

__[Friendly Id](http://rubygems.org/gems/friendly_id)__: Rails surprisingly does not come out of the box with SEO friendly urls. Friendly Id fixes this by giving human-friendly strings to your data objects. You can choose one of the existing attributes in your model or pass in a generated slug. This is super handy if you want to have public, but obfuscated, urls.

### What are your picks?

This is far from an exhaustive list, but it covers the gems I use most frequently. Now it's your turn, [let me know](http://www.twitter.com/gpxl) what gems you use to bootstrap your MVPs.
