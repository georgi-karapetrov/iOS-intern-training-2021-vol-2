# The concept
In 2007, the first iPhone, the [iPhone 2G](https://en.wikipedia.org/wiki/IPhone_(1st_generation)) was released. Music player capabilities ("an iPod on your phone") was one of its strongest selling points. However, in typical ["giant corporation"](https://en.wikipedia.org/wiki/Apple_Inc.) fashion, the phone was designed with "anti-piracy" mechanisms, meaning that one could not listen to thier own music library without using iTunes. Later, with the introduction of the iTunes Music store, Apple's initial intentions became even more clear. If you wanted convenience, you had to pay them money.

# We say no

Luckily, free services like [YouTube](https://www.youtube.com) provide their own stream of media of decent quality. With [a few rare exceptions](https://www.youtube.com/watch?v=DkiA3yydKAw), every piece of music is documented and uploaded there. Of course, being "giant corporation" themselves, Google supplies iOS users with a YouTube application. However, in [typical "giant corporation" fashion](http://4liberty.eu/wp-content/uploads/2016/02/RTR2RSIQ.jpg) there are a lot of features which are not accessible to "free" users. A [YouTube Red](https://www.youtube.com/red) subscription is required in order to be able to use the application in its full potential.

# We say no (again)

Our task is simple: we beat them at their own game. And we do this as follows:

## Create an iOS application, called 'PirateRadio'

 It allows the user to watch YouTube videos on their device.

## Wait, but there's more!

After a secret combination of gestures, it enters a 'Pirate' mode. This mode enables 'power user' capabilities which are:

* Listen to music while the device's screen is turned off
* Download and save videos on your device for offline use

## So, how we do it?

The key is in ["Knowing your enemy"](https://www.youtube.com/watch?v=4smim2MNvF8) :)). Get started with YouTube's [developer API](https://developers.google.com/youtube/). _Protip: Create a developer account if you don't already have one._ Then learn about **NSURLSession** [here](https://developer.apple.com/documentation/foundation/nsurlsession). It is the foundation we are going to build our client-server communication on.

## Before you start

Create an Xcode workspace to hold you application. It will be needed in order to integrate [CocoaPods](https://cocoapods.org/about) with our PirateRadio.

## Next up

After you've studied the YouTube API and the **NSURLSession** class, create your models. They should match the [JSON](https://www.w3schools.com/js/js_json_intro.asp) responses of the API as closely as possible. _Protip: Avoid additional properties/properties with different names in your models as much as possible._

## Playing the video

Pick a framework that already does that from [CocoaPods](https://cocoapods.org/) and integrate it with the PirateRadio. [Here](https://guides.cocoapods.org/) is how to set CocoaPods up.

## Saving the video locally

There will be a need to incorporate [another](https://media.giphy.com/media/GV3aYiEP8qbao/giphy.gif) API in order to fulfill our sacred mission. As these are usually shady and go out of order quite frequently, by the time you are attempting this, the supplied API might not be viable. Your task is to dig out a working one for the sake of presenting your application. Here's [one](https://elements.heroku.com/buttons/aymen-dev/youtube-to-mp3-api) which is working as of 8th Jun 2021.

## The James Bond part

_[classified]_

## Up to you

Investigate what needs to be done in order for an app to be able to play music while in background mode. Here's a [hint](https://developer.apple.com/documentation/avfoundation/avplayer).