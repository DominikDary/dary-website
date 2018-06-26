---
date : 2012-04-15
slug : "'2012/04/calabash-ios"
status : "publish"
title : "Calabash-iOS"
Categories : ["mobile test automation"]
---

In today's post I'm describing about how to setup [calabash-ios](http://blog.lesspainful.com/2012/03/07/Calabash-iOS/) to automate your functional end-to-end test for iOS applications. In [my previous post I](http://www.dary.de/posts/2012/03/greenhouse-application/) described about how to setup the Greenhouse application.If you are interested in how to automate an Android app, [checkout this blogpost](http://www.dary.de/posts/2012/04/calabash-android/).

For using [Calabash-ios](https://github.com/calabash/calabash-ios), you need to have access to the app source code. The XCode project must modified, which means in detail, that a http server is added through linking with the the _calabash.framework_. The Calabash client library is sending HTTP requests to this server which is executing those commands.

![Calabash-ios Architecture](/calabash-ios.png)

To get startet [github](https://github.com/calabash/calabash-ios/blob/master/README.md) contains a very detailed description, about howto setup calabash-ios in general.

Currently there are two ways about how the setup can be done:

  * Automated: using the command _calabash-ios setup_
  * Manual: detailed steps are described on the wiki

I made good experience using the automated setup, but if you identify weird things in your app during test execution, I recommend to do a manual setup. For the Greenhouse iOS app I have used the manual setup, because I have seen some weird behavior.

In the first screencast I'm showing you, about how to do the automated calabash setup with the provided script:
<iframe src="http://player.vimeo.com/video/40395001" width="500" height="400" frameborder="0" webkitAllowFullScreen mozallowfullscreen allowFullScreen></iframe>

In the second screencast, I describe all the detailed steps that needs to be done for manual the setup:
<iframe src="http://player.vimeo.com/video/40402428" width="500" height="400" frameborder="0" webkitAllowFullScreen mozallowfullscreen allowFullScreen></iframe>

The the new target has been added to the app, you can verify in the logs that after starting the app the http server on the port 37265 is bound to. The default feature folder can be created with running the command _calabash-ios gen_, that is containing the feature file and all the other Ruby related Cucumber classes.

The third screencast is showing the actual test execution:
<iframe src="http://player.vimeo.com/video/40403372" width="500" height="400" frameborder="0" webkitAllowFullScreen mozallowfullscreen allowFullScreen></iframe>

Karl Krukow, the creator of Calabash-ios, has given at the [CukeUp! 2012](http://skillsmatter.com/podcast/home/calabash-an-open-source-automated-testing-technology-for-ios-and-android) a pretty nice presentation and live demo about advanced features (like gesture (touch) recording and how these events can be played back).
