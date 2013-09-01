---
layout: post
title: "Introducing Color Palettes"
excerpt: "Colors extracted from stylesheets"
date: 2013-09-01 11:32
published: true
external-url:
---
This month I created a little web app, [Color Palettes](http://colorpalettes.gerlandopiro.com) to visualize the colors used on popular websites. The inspiration came from a discussion with [@jina](http://www.twitter.com/jina) in which we discussed how to show people the benefits of using SASS over plain HTML. 
Of course, one of the easy wins with using something like SASS is reduced duplication of code. So I thought, what if there was a tool that quickly showed how much duplication there was in their existing stylesheets. Color Palettes is the first result of that thought and a bit of weekend hackery. 
The site reads in a website's stylesheets and presents the colors grouped by number of instances found. It's extremely limited at the moment but it's still fun to throw a url at it and see what comes back. Here's what I've found from the sites indexed so far.

### Complexity is everywhere

Every stylesheet so far has shown multiple variations of the same color within a color palette. For example, it's extremely common to see white represented by the values 'white', #fff, and #ffffff.

### 50 shades of grey

Monochrome values rule everyone's color palettes. Transparent and white are almost universally the most used values in stylesheets which is interesting since one would think such basic colors would be defined at a high level within the CSS and overwritten as needed, not defined over and over again throughout a stylesheet.

### Apple has the least amount of colors and complexity

For a company renowned for it's design, [Apple](http://colorpalettes.gerlandopiro.com/colormaps/apple) sure keeps it simple on the css front with only 39 colors in 147 tags. One thing in their favor, from a colors standpoint, is that they rely on imagery a lot more than most companies.

### Is this interesting?

If you discover any other interesting insights from [Color Palettes](http://colorpalettes.gerlandopiro.com) I'd love to hear about them! You can also find the [css parsing gem](https://github.com/gpxl/DryCss) and [website](https://github.com/gpxl/colorpalettes) code on Github if you feel like it.

