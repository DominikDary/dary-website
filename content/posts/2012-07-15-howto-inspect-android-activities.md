---
layout: post
title: "How to Inspect Android Activities"
date: 2012-07-15
categories:
- mobile test automation
- calabash-android
toc: true
draft: false
---
For writing good automated mobile end-to-end tests I personally prefer to use e.g. the IDs of the elements. For doing this, you can have a look at the application's source code and analyze the corresponding *layout.xml* file.

But sometimes, if e.g. on the screen are dynamic lists like search results displayed, it is quite helpful to inspect the dialog on the mobile device that is currently displayed.
The Android platform has a tool called hierarchy viewer - which is working quite well. The full UI element tree is displayed and the properties of each element can be displayed. The drawback of this tool is, that is quite slow and on some machines with less than 4GB RAM it is unusable.

For Calabash-Android I implemented a command that inspects the current dialog and returns about each UI view component the corresponding class name, the Android ID (name, defined in the layout.xml file) and for some elements the text:

{% gist 3113570 %}

In combination using the interactive Ruby shell, which I have described in my [last blog post](http://dary.de/2012/07/speed-up-the-development-of-calabash-android-tests/) , this is quite powerful and is speeding up the test development a lot. The command for the shell is:

	performAction('inspect_current_dialog')
