# FullScreenTest

## A simple sample project for extended height status bars

This project contains a very simple, full height application. 

My question is: What is the best practice to handle an extended height status bar, i.e. with the extra status bar presented when a phone call or a VoIP app is present, or when the personal hotspot feature is activated?

Is the `UIApplicationWillChangeStatusBarOrientationNotification` notification (or the corresponding delegate method of `UIApplication` the right way to do it, or am I overlooking something obvious?

## To try

The easiest way is just to enable the personal hotspot, or to start an app which records audio in the background.

Then start this app on a phone. In the simulator, you can start the app, and simulate an incoming phone call.

You will see that the text is hidden. In non-fullscreen apps, this is handled automatically by the system, by resizing the view controllers view frame. This does not seem to be the case if `wantsFullScreenLayout` is set to `YES`
