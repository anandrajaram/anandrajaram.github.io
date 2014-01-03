---
author: admin
comments: true
date: 2011-02-03 14:30:34+00:00
layout: post
slug: the-many-quirks-of-email-marketing
title: The many quirks of Email Marketing
wordpress_id: 181
categories:
- email marketing
- lifecycle marketing
tags:
- email marketing
- mailchimp
---

If you have tried to send a decent looking HTML email as part of your [lifecycle marketing](http://blog.bronto.com/2009/04/16/lifecycle-marketing-whats-love-got-to-do-with-it/), you are probably aware of the painful details that you to worry about. The whole point of Lifecycle marketing is to get your message hyper-personalized and relevant to your customer, based on which stage of the funnel they are in. In addition to figuring out the different types of customers, which stage they are at and what to message to them at that stage, you have also probably figured out [what SPF means](http://en.wikipedia.org/wiki/Sender_Policy_Framework) ( no, not the kind you put on at the beach) and can likely teach a Microsoft engineer about how Microsoft[ Outlook renders emails vastly differently between 2003 and 2007](http://blogs.sitepoint.com/2007/01/10/microsoft-breaks-html-email-rendering-in-outlook/). Ditto about how the same email shows up differently between Hotmail, Yahoo and Gmail. ESPs such as [Campaign Monitor and MailChimp provide tools](http://stackoverflow.com/questions/1018078/testing-html-email-rendering) that you can use to verify how your email will show up in a variety of different mail clients.

But I just realized the other day (not surprising on hindsight) that there is another variable in this equation. **Your browser**. Here is the email that I was designing (with the images turned on).

![Email with images](http://www.startupproductmanager.com/images/email-with-images.png)

Like any good marketer, I setup alt-text in my email so that users see meaningful content when images are disabled (and every client except Apple Mail disables it by default). Heck, I even phrased it such that I nudged the user to enable images. But for some mysterious reason, the alt text didn't show up in Gmail.

![Gmail chrome no alt text](http://www.startupproductmanager.com/images/gmail-chrome-no-alt-text.png)

After some investigation (and thanks to some useful pointers from MailChimp), it turned out that the issue does not have to do with Gmail but with Chrome. The same email (received in Gmail), displays Alt-Text perfectly fine in FireFox. Here is the same email in Firefox, with all the ALT-Text goodness.

![Gmail firefox](http://www.startupproductmanager.com/images/gmail-firefox.png)

Ah, well, if I had a dime for every HTML email quirk, I'd probably be Bill Gates (Whoa, is that how he became the richest man, haha)? But Wait, there is more.

**Chrome for Gmail Does show Alt-Text in Gmail, Sort of, sometimes**

It is not as if Chrome doesn't always show the Alt-text when rendering images at Gmail. It actually does show it, in some of the cases. You can tweak your alt+text length and figure this out by trial and error. This is a [documented bug for Chrome](http://code.google.com/p/chromium/issues/detail?id=51533) . From a Google Search, it looks like I am coming a bit late to this party, and the issues has been known for a few years now. I am still so aghast, I had to write about this.

Good luck getting those emails nice, pretty and accessible. May the force be with you.
