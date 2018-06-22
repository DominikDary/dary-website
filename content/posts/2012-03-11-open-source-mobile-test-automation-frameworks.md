---
date: 2012-03-11
layout: post
title: Open Source Mobile Test Automation Frameworks
categories:
- mobile test automation
styles: [data-table]
toc: true
draft: false
---

The mobile market is changing. In the past a lot of mobile solutions has been created and a lot of them has been used to gather experience in the mobile field.
Now more and more companies like [car manufacturers](http://servicingstopbmw.co.uk/news/bmw-expanding-in-the-mobile-apps-sector/) or banks ([PayPal](https://personal.paypal.com/us/cgi-bin/?&cmd=_render-content&content_ID=marketing_us/mobile_payments), [Barclays](http://www.bbc.co.uk/news/technology-17040702))are creating mobile solutions that really have an impact on their main business.
If you look e.g. at [eBay's mobile facts](http://mobile.ebay.com/wp-content/themes/platformpro/downloads/eBay%20Mobile%20Collateral%202_16_2012.pptx), the numbers are just impressing:

 + 2011 there was a transation volumne of 5 billion USD worldwide
 + 1 million Listings every weeks are done via mobile
 + 176 Number of dollars spent every second through mobile purchases


From a test automation perspective, I'm looking into this area from a functional end-to-end testing perspective, there are different open source tools available to write automated tests for iOS and Android:


Overview about Open Source Test Automation Frameworks:

Framework | Native Platforms |	Mobile Web |	Homepage |	Emulator |	Device
:----------|:------------|:----------|:----------|:------------|:----------
Nativedriver |	iOS and Android	|-	| [http://goo.gl/ZnhnN](http://goo.gl/ZnhnN) |	X |	X
Calabash |	iOS and Android |	- |	 [http://goo.gl/F52W4](http://goo.gl/F52W4) |	X |	X
MonkeyTalk |	iOS and Android |	- |	[http://goo.gl/JSrIt](http://goo.gl/JSrIt) |	X |	X
Frank |	iOS |	- |	[http://goo.gl/1dmkA](http://goo.gl/1dmkA) |	X |
Robotium |	Android | 	- |	[http://goo.gl/OiAc9](http://goo.gl/OiAc9) |	X |	X
KIF |	iOS |	- |	[http://goo.gl/oBTHH](http://goo.gl/oBTHH)	|	X |
Zuchini |	iOS |	- |	[http://goo.gl/umvnY](http://goo.gl/umvnY)	| X |	X
Selenium |	- |	iOS and Android	 | [http://goo.gl/RIqj6](http://goo.gl/RIqj6) |	X |	X


The list shows how many frameworks are available and all of them have their benefits. I think it is interesting that currently it looks like that there is no 'killer framework' out there like 'Selenium' for the web with its infrastructure component Grid2. In the upcoming months I will write some detailed blog posts about how to use the different frameworks in practice.

In the list above I probably have overseen a framework, so please, add the missing one to the comments and I will add it to the list.
