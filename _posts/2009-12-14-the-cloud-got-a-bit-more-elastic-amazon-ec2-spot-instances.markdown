---
author: admin
comments: true
date: 2009-12-14 18:44:57+00:00
layout: post
slug: the-cloud-got-a-bit-more-elastic-amazon-ec2-spot-instances
title: The Cloud got a bit more elastic - Amazon EC2 Spot instances
wordpress_id: 22
categories:
- technology
tags:
- cloud
---

At the [Xconomy Cloud^3 conference and unpanel](http://www.xconomy.com/boston/2009/12/11/thank-you-to-our-cloud3-speakers-seeders-sponsors-and-underwriters-and-an-update-on-speaker-slides/) last week, there was a lot of great discussion around the Cloud's cost economics and at what point the Cloud becomes more expensive than a in-house data center. As part of the unpanel discussion, I had mentioned that cost models will continue to evolve in the cloud and that we are in the very early stages.

And here it is, the [Amazon Ec2 Spot pricing](http://aws.typepad.com/aws/2009/12/ec2-spot-instances-and-now-how-much-would-you-pay.html). The concept is seemingly straightforward (with a somewhat unexpected twist). You can bid for "Spot Instances" where you specify the price you are willing to pay for an EC2 instance. To quote the AWS blog "As requests come in and unused capacity becomes available, we'll evaluate the open bids for each Region and compute a new Spot Price for each instance type". And here is the twist. After that **we'll terminate any Spot Instances with bids below the Spot Price**, and launch instances for requests with bids higher than or at the new Spot Price. The instances will be billed at the then-current Spot Price regardless of the actual bid. I don't know why the instances would have to be terminated, rather than a simple re-calculation of the price of running the instance, but this seems like a fun experiment.

To be able to fully take advantage of this kind of flexibility being offered, your application (actually I should background jobs) would have to be totally stateless and be able to resume from any where in a workflow. Queuing mechanisms such as SQS come in handy. Like I mentioned in my talk, it is probably good design anyway to be stateless. And of course, please don't run your web server or user-facing applications in a Spot instance. That is a guaranteed way to get fired.

All in all, I think this is more of a pricing experiment from Amazon's perspective, more than anything else. Getting every additional dollar out of your excess capacity is a centuries old problem (think free business cards from VistaPrint), and I'd be interested in knowing how this pans out for Amazon and how Spot prices compare to traditional prices.
