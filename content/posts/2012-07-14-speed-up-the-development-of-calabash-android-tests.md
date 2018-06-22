---
layout: post
title: "Speed up the Development of Calabash-Android Tests"
date: 2012-07-14
categories:
- mobile test automation
- calabash-android
toc: true
draft: false
---

In one of my [previous blog posts](http://dary.de/2012/04/calabash-android/) I described about how to use Calabash-Android in general.
In today's post I'm describing about how to speed up the development of automated mobile tests using Calabash-Android using and mostly configuring the interactive Ruby shell (IRB).

IRB is a shell allows the execution of Ruby commands with immediate response, experimenting in real-time. This is pretty useful if you are about to automate an Android application screen that is part of an flow and you are in the process of finding for the UI elements the right commands e.g. where sometimes it is easier to use find Elements by text and sometimes you can use the Android element names. Especially if you are using customized UI components, then sometimes this can be tricky.

To speed this process I'm using the IRB shell, that is already preconfigured in Calabash-Android.
Important are the files

* .irbrc (which configures the IRB shell) and
* irb_android.sh (the script that is starting the irb shell)

which can be found [here](https://github.com/calabash/calabash-android/tree/master/ruby-gem/features-skeleton).

I started with this original templates and customized them:
{% gist 3110764 %}

In the file *.irbrc* the main change is in the last line, the command, to connect to the test server, which is running on the device / emulator.
In the file *irb_android.sh* I added the command to start the Android instrumentation, which will start the calabash-android test server on the phone / emulator and as well the application under test (AUT).
The port and as well the package of the AUT can be configured, especially making the package configurable makes it easier if you are writing tests for different apps.

The IRB shell is started using the command:

	./irb_android.sh com.springsource.greenhouse.test

Now you can send calabash commands e.g. like press a button with the text "Sign In":

	performAction('press_button_with_text', 'Sign In')

If you would like to get an overview what commands are by default available, you find them on [github](https://github.com/calabash/calabash-android/tree/master/ruby-gem/lib/calabash-android/steps)

The above described approach is working under the assumption, that the *Test.apk* (which contains the Calabash-Server) and your application to test are already installed on your device/emulator. The *Test.apk* file is created dynamically at runtime while executing the calabash-android tests. The generated file is then located under the folder *features/support/*.
