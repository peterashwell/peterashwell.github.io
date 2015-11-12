---
layout: post
title:  "Oh boy Ionic"
date:   2015-10-25 21:00:00
categories: ionic android emulator
---

Had an issue where the app would crash immediately after being started. The emulator would load fine, but the app would crash. Was not impressed.

Installed adb, the android debugger, from android tools and checked the logs. Found an error related to some sanity check in Chromium:

```[FATAL:gl_surface_android.cc(58)] Check failed: kGLImplementationNone != GetGLImplementation()
```

Googling led very slowly to this solution: <http://stackoverflow.com/questions/29235649/cannot-get-crosswalk-helloworld-example-to-work>

Basically, if you don't check the 'use host GPU' box it just won't work. Thanks for putting that in the n00b guide there ionic.
