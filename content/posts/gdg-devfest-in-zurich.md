---
title : "GDG Devfest in Zurich"
date : 2012-10-20
status : "publish"
slug : "2012/10/gdg-devfest-in-zurich"
Categories : ["mobile test automation", "mobile testing", "calabash-android", "calabash-driver"]
---

Yesterday and today I attended the Google Developer Group (GDG) DevFest in Zürich and I really enjoyed it! I have seen good presentations, met really nice people and I had great discussions.
This afternoon I did a presentation about how to automate native Android apps using [Calabash-Driver](http://calabash-driver.github.com) and how to leverage an existing Selenium Grid2 architecture to allow scaling and parallel testing.

Here you find my slides of today's presentation:
<iframe src="http://www.slideshare.net/slideshow/embed_code/14814376" width="427" height="356" frameborder="0" marginwidth="0" marginheight="0" scrolling="no" style="border:1px solid #CCC;border-width:1px 1px 0;margin-bottom:5px" allowfullscreen> </iframe>

For the GDG DevFest presentation I used the [Greenhouse application](http://www.dary.de/posts/2012/03/greenhouse-application/) to showcase about how to write an automated Android end-to-end test. Please keep in mind that this showcase was created mainly to demonstrate, how Android app automation looks like in practice. This means the super class of the test case is starting the Calabash-Driver Server automatically. In a scenario where the Selenium Grid would be used, this component is typically started per shell script.

The actual code of the showcase is located at [Github](
https://github.com/DominikDary/gdg-devfest-zrh). To get started please follow the steps described in the [Greenhouse application](http://www.dary.de/posts/2012/03/greenhouse-application/) blog post. For executing the scripted test you need first to install both *apk files*, that are located in the github project in the [*download*](https://github.com/DominikDary/gdg-devfest-zrh/downloads) section. After starting the emulator, the test can be executed by executing the TestNG test.

[Update 1. November 2012]
The full talk was recorded and is now available on YouTube.
<iframe width="560" height="315" src="http://www.youtube.com/embed/BExAKDslV9I" frameborder="0" allowfullscreen></iframe>

My colleague Tim Messerschmidt ( Developer evangelist at PayPal) attended the DevFest as well and introduced *PayPal Access*. If you are interested in this topic, I recommend to checkout his [blog post](http://www.timmesserschmidt.de/2012/10/access-beim-devfest-zurich.html).
