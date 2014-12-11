---
layout: post
title: "SSL all the things (for free) : A How To Guide"
date: 2014-12-10 21:30
published: true
external-url:
categories: "development"
image: 'ssl-all-the-things.jpg'
---
<p class="text-center">
  <img src="/images/ssl-all-the-things.jpg">
</p>

If you're running any kind of business online, you're going to want an SSL (https) enabled domain. Not only will this provide your users with a secure connection between themselves and your servers (to protect their sensitive data), but [Google has announced SSL support as one of their ranking metrics](https://googlewebmastercentral.blogspot.com/2014/08/https-as-ranking-signal.html) that will grow in strength over time. Gumroad also notes that [SSL leads to higher conversion rates](https://help.gumroad.com/customer/portal/articles/1622004-how-do-i-set-up-the-gumroad-overlay-)

###So why doesn't everyone have SSL on their site?

Until recently, getting an SSL certificate set up was an expensive and down right confusing process even for those of us well versed in internet sorcery. The process involves generating keys on a web server, sending them to an SSL authority, waiting for a certificate to be sent back, then installing the certificate on your web server. And that's for the most simple scenario. Good luck if you want to support multiple domains and subdomains at the same time. Oh, and they expire too so you get to go through the process all over again every few years!

Fortunately someone sought to address the complexity and offer a simple (and free) solution. That someone is [CloudFlare](https://www.cloudflare.com), and the product is called flexible SSL. Below I will detail how to set up flexible SSL for yourself by using my own domain as an example. 

##Let's get started

###[Signup with CloudFlare](https://www.cloudflare.com/sign-up)

<p class="text-center">
  <img src="/images/ssl-create-account.png" class="img-thumbnail">
</p>

### Add your website domain

CloudFlare will scan your domains current DNS settings making this step a simple click and wait.

<p class="text-center">
  <img src="/images/ssl-add-website.png" class="img-thumbnail">
</p>

### Configure your DNS records

The important ones to note are the "A" and "CNAME" records, these should be showing the "On CloudFlare". Most likely you just need to click the button to continue setup.

<p class="text-center">
  <img src="/images/ssl-configure.png" class="img-thumbnail">
</p>

### Choose your plan

The Free plan will suffice! Go with the default settings here, you can always revisit these later if you want.

<p class="text-center">
  <img src="/images/ssl-choose-plan.png" class="img-thumbnail">
</p>

### Update your DNS

CloudFlare will now show you which domain name servers to use. Jump over to your domain registrar to update your DNS host records. _duke.ns.cloudflare.com_ and _pola.ns.cloudflare.com_ in the screenshot below. 

<p class="text-center">
  <img src="/images/ssl-name-servers.png" class="img-thumbnail">
</p>

Sometimes finding the right screen on your domain registrars website is half the battle! My registrar, Namecheap, hides it under "Transfer DNS to Webhost".

<p class="text-center">
  <img src="/images/ssl-update-dns.png" class="img-thumbnail">
</p>

### The waiting is the hardest part

Once your DNS records have been updated, you're done! Your new settings will take a while to spread across the internet so just be patient and check back after 24 hours.

##Pat yourself on the back!

SSL is one of those unsexy yet crucial aspects of website development. Cloudflare has made it a lot easier and a lot less expensive to provide the security your customers deserve. If this still more effort than you want to put in (and who could blame you?), take a look at [Taskitt](https://www.taskitt.com), web development as a service.
