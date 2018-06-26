---
title : "Mobile webdriver Selendroid"
date : 2013-11-21
status : "publish"
slug : "'2013/11/mobile-webdriver-selendroid"
Categories : ["mobile test automation", "mobile webdriver", "w3c", "Android", "selendroid"]
---

![selendroid logo](http://selendroid.io/images/selendroid-logo.png)

In this blog post I would like to write again about mobile test automation.
In the last months I spent a lot of my time working on a new test automation framework: [Selendroid](http://selendroid.io) - a [mobile WebDriver](http://seleniumhq.wordpress.com/2013/08/28/mobile-webdriver/) implementation for native and hybrid Android apps.

Selendroid is an implementation of the [Selenium WebDriver JSON Wire protocol](http://code.google.com/p/selenium/wiki/JsonWireProtocol), which is about to become a [W3C Standard](http://www.w3.org/TR/webdriver/).


### Main features of selendroid are:

* Full compatibility with the JSON Wire Protocol.
* No modification of app under test required in order to automate it
* Testing the mobile web using built in Android driver webview app
* Same concept for automating native or hybrid apps
* UI elements can be found by different locator types
* Gestures are supported: [Advanced User Interactions API](http://selendroid.io/gestures.html)
* Selendroid can interact with multiple Android devices (emulators or hardware devices) at the same time
* Existing Emulators are started automatically
* Selendroid supports hot plugging of hardware devices
* Full integration as a node into [Selenium Grid](http://selendroid.io/scale.html) for scaling and parallel testing
* Multiple Android target API support (10 to 19)
* Built in [Inspector](http://selendroid.io/inspector.html) to simplify test case development.

### In Action

I order to keep that example as simple as possible, I have created a [small demo project](Github](https://github.com/selendroid/demoproject-selendroid) in which the [selendroid-test-app](https://github.com/selendroid/selendroid/tree/master/selendroid-test-app) is used, the app that we use to verify that selendroid itself works fine.

### More Details?

The source is hosted at github: [http://github.com/selendroid](http://github.com/selendroid).

The Documenation is available at [http://selendroid.io](http://selendroid.io).

<iframe src="http://de.slideshare.net/slideshow/embed_code/28516739" width="427" height="356" frameborder="0" marginwidth="0" marginheight="0" scrolling="no" style="border:1px solid #CCC;border-width:1px 1px 0;margin-bottom:5px" allowfullscreen webkitallowfullscreen mozallowfullscreen> </iframe>

Happy mobile testing!
