
Android Native EGL example
==========================

This project demonstrates how to combine Java application with native
C/C++ code for OpenGL rendering on Android 2.3 and newer.  It shows
how to do rendering without GLSurfaceView and GLSurfaceView.Renderer
Java classes.  The solution gives full control of the rendering for
the native code while still allowing the convenience of using Java for
calling Android APIs.

Java part of the sample application is responsible for the main UI and
application lifecycle.  It creates empty SurfaceView and passes that
to the native code.  Native code uses that for OpenGL rendering.  The
application is running standard Java activity and not the
NativeActivity.

Native code starts a new thread using pthreads API to execute
rendering code.  It uses EGL API to set up rendering context for the
thread.

![screenshot](http://i.imgur.com/qTfiE.png)

Requirements
------------

Android API level 9 and Android NDK r5 


Acknowledgments
---------------

The EGL setup code was adapted from Android NDK native-activity sample.

The OpenGL cube was adapted from Android SDK Graphics ApiDemos.

