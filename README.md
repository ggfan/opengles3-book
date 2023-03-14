OpenGL ES 3.0 Programming Guide
===============================

This repository contains the sample code for the OpenGL ES 3.0 Programming Guide by Addison-Wesley Professional (http://www.opengles-book.com). 

## Platforms ##
The sample code for the OpenGL ES 3.0 Programming Guide currently builds on the following platforms:

* Microsoft Windows 
* Linux X11
* Android 4.3+ NDK (C/C++)
* Android 4.3+ SDK (Java)
* iOS7

Instructions for building for each platform are provided in Chapter 16, "OpenGL ES Platforms".

## Authors ##
Dan Ginsburg<br/>
Budirijanto Purnomo<br/>
Previous contributions: Dave Shreiner, Aaftab Munshi

## Reader Contributions ##
We would like to thank the following people for their contributions to the source code:
* Javed Rabbani Shah for contributing the Android SDK port as well as helping with the NDK port
* Jarkko Vatjus-Anttila for contributing the original Linux/X11 port for the OpenGL ES 2.0 Programming Guide
* Eduardo Pelegri-Llopart and Darryl Gough for contributing the Blackberry Native SDK port for the OpenGL ES 2.0 Programming Guide (we have not yet ported the ES 3.0 book to a Blackberry platform)

## Android Tips ###
1.  Windown connection:
* Surface handle from Java side (SurfaceView, Surface) when it is created.
* NDK API ANativeWindow_fromSurface(env, JavaSurfaceObject) returns a native window.
* OpenGL context can come to play.
2. GameActivity secrete steps.
* `hasCode` in AndroidManifext.xml can not be false
  (for NativeActivity it should be false if app does not derive class from NativeActivity).
  This is because that GameActivity is outside the framework, app will always have java byte code.
* Static lib approach does not support C app, it has to be C++ app
* GameActivity can be the startup Activity (means that there is no application hand created Java code).


