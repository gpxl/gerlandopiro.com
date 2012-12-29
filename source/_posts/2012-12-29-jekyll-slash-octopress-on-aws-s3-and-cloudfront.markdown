---
layout: post
title: "Jekyll/Octopress on AWS S3 &amp; CloudFront"
date: 2012-12-29 09:53
published: true
sharing: false
external-url: http://blog.alexbrowne.info/how-i-made-my-blog-faster
---
Alex Browne justifies his move from a dynamic site on Heroku to a static site on AWS by detailing performance improvements. But the REAL benefit in my opinion is here:
> As for the price? Well over the course of testing I probably sent more than one million requests to the CloudFront servers and transferred around a gigabyte of data. According to the pricing charts, this will cost me a measly single dollar. Not bad at all, especially considering that’s far more traffic than I expect to get in a typical month.
The bigger benefit is dropping costs from $35/mo. for a minimally sufficient Heroku Dyno to less than $1/mo. on bare AWS. I plan on replicating his efforts and detailing my own experience in a future post.
