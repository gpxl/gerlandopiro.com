---
layout: post
title: "Scrypt Mining with a Gridseed ASIC, Raspberry Pi, and Scrypta"
excerpt: "Indirect Bitcoin mining made easy."
date: 2014-03-02 21:30
published: true
external-url:
categories: bitcoin
---
Dedicated hardware (ASICs) for scrypt mining finally hit the market in force last month with the release of the [DualMiner](http://www.dualminer.com) and [Gridseed](http://www.gridseed.com) ASIC mining devices. As expected, early adopters experienced a lot of pain with weak software, faulty hardware, and poor vendor support. However, things quickly improved at the same time an increase in distribution brought about better service from vendors and lower prices. The release of a dedicated [Raspberry Pi distribution for Gridseed devices](https://litecointalk.org/index.php?topic=9908.0) finally made ASICs a viable alternative to GPU mining for most people.

In order to truly understand what these devices are about, I purchased a Gridseed from [ZoomHash](http://zoomhash.com), an unloved [Raspberry Pi](http://en.wikipedia.org/wiki/Raspberry_Pi) snagged from a coworker, and set out to see how ASICs compares to GPU mining.

<div class="panel panel-default">
  <div class="panel-heading panel-title">Gridseed in Hand</div>
  <div class="panel-body text-center">
    <img src="/images/gridseed.jpg" alt="Gridseed">
  </div>
  
</div>

Setting up the Raspberry Pi was a simple matter of copying Scrypta to a SD card and plugging in the Pi. Once booted a web interface, located at the Pi's ip address, allows configuration of mining pools and displays mining status information. It's a well designed interface that's very nice to use.

<div class="panel panel-default">
  <div class="panel-heading panel-title">Simply Pretty</div>
  <div class="panel-body text-center">
    <img src="/images/scripta.png" alt="Scripta">
  </div>
</div>

Once the Pi is ready, all that's left to do is to plug the Gridseed into the Pi with a USB cable and power on both the Gridseed and the Pi.

That's all there is to it! Once booted, you should see the Gridseed hashing at 3.6mh/s on your pool of choice. Better yet, it will draw less than 9W of power while doing so, an order of magnitude less than a GPU mining card.

Adding more Gridseeds gets slightly more complicated in that you will need to add a USB hub since each device requires a port. Each device requires their own power source as well. Using a simple power brick doesn't scale very well and using a larger power supply requires hacking together your own cables. However, I have no doubt that within the next 30 days a number of out of the box solutions will be on the market.

Overall my experience with Gridseed Scrypt ASICs has been a positive one. So much so that I've started downsizing my GPU mining in favor of them.
