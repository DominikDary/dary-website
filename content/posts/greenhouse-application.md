---
date : 2012-03-12
slug : "'2012/03/greenhouse-application"
status : "publish"
title : "Greenhouse Application"
Categories : ["mobile test automation", "Spring Greenhouse"]
---

In my [past blog entry](http://www.dary.de/posts/2012/03/open-source-mobile-test-automation-frameworks/) I listed different Open Source Frameworks that can be used for mobile testing on Android and iOS. For showcasing the different frameworks, I will use the Open Source project Greenhouse that SpringSource has created some while ago to:


Serve as a open-source, public-facing reference and driver for Spring technology, including Spring MVC, Security, Integration, and the new [Spring Social](http://www.springsource.org/spring-social) and [Mobile](http://www.springsource.org/spring-mobile) projects.

For making the demonstration easier, I have forked the corresponding projects on Github and in the following lines you find all the details you need to follow to setup everything:

  * [greenhouse](https://github.com/DominikDary/greenhouse)
Main web application which provides the data for the mobile apps.
  * [greenhouse-iphone](https://github.com/DominikDary/greenhouse-iphone)
The code of the iPhone app.
  * [greenhouse-android](https://github.com/DominikDary/greenhouse-android)
The code of the Android app.

SpringSource has created a [guide](http://www.springsource.org/greenhouse/guide) about how to setup the development environment. The main reason for creating the fork was the data initialization, for doing this you need

  * to clone the greenhouse project and
  * to update the [test-data.sql](https://github.com/DominikDary/greenhouse/blob/1946f0e7c460eda7265f22cedf2c3bd93a75833b/src/main/java/com/springsource/greenhouse/config/test-data.sql).


**Running the webapp**
The webapp can be started using Tomcat from the command line by invoking the Tomcat 7 Maven plugin:
_mvn clean install t7:run_
The webapp can be found under: [http://localhost:8080/greenhouse](http://localhost:8080/greenhouse) where you can login with the following details (in the above mentioned sql file you find other credentials as well):
Username: _craig@habuma.com_
Password: _freebird_

**Running the Android app** (Details are taken from the greenhouse-android wiki)
Build and Run the Greenhouse for Android app:

	$ _cd greenhouse-android_
	$ _mvn clean install_
	If your favorite Android emulator is started:
	$_ mvn android:deploy_

In this screencast I describe how the greenhouse environment is setup:
<iframe src="http://player.vimeo.com/video/38326270" width="500" height="400" frameborder="0" webkitAllowFullScreen mozallowfullscreen allowFullScreen></iframe>
