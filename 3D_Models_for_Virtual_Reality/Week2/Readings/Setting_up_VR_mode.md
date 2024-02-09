# Setting up VR mode

## Overview

Setting up Unity to work in VR is often quite straightforward, but there can be some difficulties based on what platforms you use. 

If you run into problems this can be one of the hardest parts of all of VR development, but don't panic! You will be able to sort out the problem, and you might be able to fix it yourself, but don't feel like you are on your own. There is a lot of information available online, and you can often find the answer with a quick web search. But the best thing to do is use the community of learners on this course. If you are having troubles, ask questions on the forum. If you are having a problem, it is very likely that some one else will have had the same problem, and probably solve it. Even if not, other learners and our Teaching Assistants will be available to help. 

When you set up your environment you need to think about two things:

### The headset you have. 

This is the most obvious piece of hardware, but it also influences the software plugins that are needed. Luckily setting these up is mostly fairly straightforward, and will be explained below. 

### The computer or device that will drive your headset. 

If you are using a high end system like an Oculus Rift, HTC VIVE or Windows MR headset, your app will run on the computer that you are using to develop it, and so it doesn't need any particular set up. You just need to make sure that your computer is capable of driving the headset. At the moment this probably means it has to be a high specification Windows machine as Mac and Linux are not really supported (though, at least for Mac, this is likely to change soon, given [Apple's announcement in September](https://www.apple.com/uk/apple-events/september-2017/)). 

For mobile VR the software will run on your phone. This makes it a bit more complex because your software is running on a different device from the computer you are developing on. It also means you need to have an extra set up step that let's you run software on the phone. This can be quite tricky, but it  is something that all mobile game developers have to do, so there is quite a lot of information available about how to do it. We will go through the details below. 

## Setting up Unity for your device

This section will guide you through setting up unity for the device you will be using to run VR, which will either be a PC or a mobile device. 

This will involve 2 steps:

1. install additional software needed to run the device
2. set the builds settings to the correct device. You access from the File menu->Build Settings and they allow you to choose different software platforms. 

### Setting up for PC development

If you are developing on a PC for a tethered device like Oculus Rift or HTC VIVE you are in luck, there is very little to do. By default Unity is set up to develop for a PC and you don't need to install any extra software. 

If you are developing for Windows Mixed Reality, you need to make sure that the build settings are correct, because it Windows MR only works on the latest version of Windows. You can find the instructions in the first part of this article:

https://developer.microsoft.com/en-us/windows/mixed-reality/unity_development_overview

Otherwise, the setup is easy, and you can skip to the next section on setting up VR. 

### Setting up for an Android Phone/Oculus GO

You can set up an android phone for GearVR, Oculus GO, Google Daydream or Google Cardboard development. This article gives an overview:

https://docs.unity3d.com/Manual/android-GettingStarted.html

and here:

https://docs.unity3d.com/Manual/android-sdksetup.html

This article from our blog about Oculus GO development details some of the steps, which are also useful for other Android devices:

https://medium.com/virtual-reality-virtual-people/setting-up-unity-for-oculus-go-development-43d3e8c12f59

If you are using a normal phone with Google Cardboard, you should follow these instructions:

https://developers.google.com/cardboard/develop/unity/quickstart

For all of this to work, you need to selected the android build support option when you installed Unity. It should be selected by default, but if you didn't select it, you will need to re-install. 

The first thing to do is install the android SDK, this is the software platform that allows you to develop for android devices on your computer. It works for all types of android development, not just unity, so it includes installing things that that seem quite distant from unity development, but don't worry. Once installed you don't need to worry about these other things, just unity.

The basic process is:

1. Download and install the Android SDK. You don't need to use Android Studio, but you need the software so that Unity works. 
2. Enabling USB debugging on the device (details are here: https://docs.unity3d.com/Manual/android-sdksetup.html)
3. Open File->Build Settings and select "Android". If Unity can't find the Android SDK you will need to set the location of the Android SDK file by going to Unity > Preferences > External Tools. (This is the folder in which you installed the android SDK. 
4. Plug your android phone into your computer using a USB cable. 
5. Hit play. It will take a long time to start up first time, but should install and run your app on the phone. 

If you manage to do all of these steps you are ready to turn on VR mode (see below). 

If you run into trouble look at this page and check you have followed all of the instructions. 

https://docs.unity3d.com/Manual/android-sdksetup.html

Also, check this page that lists common problems and their solutions:

https://docs.unity3d.com/Manual/TroubleShootingAndroid.html

If all else fails, as we said above, try the course forums. 

### Setting up for an iOS phone

You can use an iPhone with Google Cardboard for VR development, if you have a Mac. This is the least well supported option, so we don't recommend it. 

There is an overview of iOS development in Unity:

https://docs.unity3d.com/Manual/iphone-GettingStarted.html

For all of this to work, you need to selected the iOS build support option when you installed Unity. It should be selected by default, but if you didn't select it, you will need to re-install. 

For iOS VR you will need to set up Google Cardboard, you can use these instructions here:

https://developers.google.com/cardboard/develop/unity/quickstart

Setting up iOS development is similar to android, but you also have to set yourself up as an official iOS developer with apple (and pay). Which can be tricky. 

The first thing you need to do is install [Xcode](https://developer.apple.com/xcode/) from the mac app store. You won't be using it directly, but you need it to run apps on an iPhone. 

Next, you need to register as an iOS developer. Unity provides some helpful instructions here:

https://docs.unity3d.com/Manual/iphone-accountsetup.html

Once you have Xcode, and an iOS developer account you can open File->Build Settings and select "iOS". 

You can then plug in your iPhone to your Mac with a USB cable. 

If you do that, pressing "play" in unity, will open up Xcode. This will build the project (which will take a long time, the first time you do it) and install it on the phone. At that point it will run on the phone. This will take quite a long time the firs time you do it, but be patient. 

If it fails to run the first time, try hitting play again (it sometimes takes so long to build on the first run that it fails). If it fails a second time check out Unity's [iOS trouble shooting page](https://docs.unity3d.com/Manual/TroubleShootingIPhone.html), or post your problem to the course forum. 

## Setting up VR mode

If you have development set for your device, getting it working with VR is generally a lot simpler. It consists of two steps:

1. Installing the software needed for your HMD/VR platform (details for each platform below, but increasingly these are built into unity by default)
2. Setting up VR mode. This is as simple as going to either File->BuildSettings and pressing the "Player Settings" button or Edit Menu->Project Settings->Player. Both will take you to the same window. You need to go to Other Settings and select "Virtual Reality Supported". You will then need  to choose which SDK you would like to use, either from the SDKs list below the check box, or if your option isn't there, add it with the "+" button (see image below). How many options you have will depend on which SDKs you have installed below, but you need to choose the one that corresponds to your device (we will explain below for each one).

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/hm-J8NLwEee3YgrjV0GSxA_31f5c6d1028e612039261cd5ddbccd0b_Screen-Shot-2017-11-26-at-21.16.32.png?expiry=1707523200000&hmac=yqKoq_SlFc4Lw9kbcqkO5O3Vrk4zsxUAV1_kC8uYIE8)

For more information, the VR tutorials section are a good place to start for VR mode:

https://unity3d.com/learn/tutorials/topics/virtual-reality

and in particular the getting started page (though it is a bit old):

https://unity3d.com/learn/tutorials/topics/virtual-reality/getting-started-vr-development?playlist=22946

The manual pages give more detailed instructions:

https://docs.unity3d.com/Manual/VirtualReality.html

https://docs.unity3d.com/Manual/VROverview.html

They give instructions on setting up a number of different VR devices:

### Oculus Rift/GearVR

Unity already comes with the Oculus SDK installed so you don't need to install any other software to develop for either Rift or GearVR. Just select "Oculus" in the SDK section when turning on VR mode (see above). If you are using GearVR, you need to make sure that you set up Android development as explained above. 

You will need to have installed the Oculus software for the Rift, but you are likely to have done that when you first bought your Rift. 

There is more information on the unity site:

https://docs.unity3d.com/Manual/VRDevices-Oculus.html

the oculus site also gives advice:

https://developer.oculus.com/documentation/unity/latest/concepts/book-unity-gsg/

### HTC VIVE

To work with the HTC VIVE you need to use the OpenVR SDK, which is included. You will also need to install the [Steam](http://store.steampowered.com/) and [SteamVR](http://store.steampowered.com/steamvr) apps (but you probably have already done that if you own a VIVE)

Setting up OpenVR development is explained in more detail here:

https://docs.unity3d.com/Manual/VRDevices-OpenVR.html

The SteamVR package provides additional functionality. 

https://www.assetstore.unity3d.com/en/?&_ga=2.236317057.1826221989.1499533961-1785571284.1389631888#!/content/32647

When you enable VR support you should choose the "OpenVR" SDK

### Windows Mixed Reality

Windows mixed reality is built into both Windows and Unity, but it is pretty recent (october 2017) so you need to make sure you have up to date versions of both. That means the Windows 10 Fall Creators Update 2017, or later and Unity version 2017.2 or later. You should select the "Windows Mixed Reality" when you turn on VR support. 

You can get more details here:

https://developer.microsoft.com/en-us/windows/mixed-reality/unity_development_overview

### Google Daydream and Cardboard

Google Cardboard is a very simple platform which works with most android phones and also iPhones. Google Daydream is a much more advanced version which works only on certain android phones. Both have a common SDK for development, called googleVR,, which is included in the latest versions of Unity. When you turn on VR support you should select "Cardboard" as your SDK or "Daydream" if you device supports it. 

This is Unity's documentation on how to set up GoogleVR:

https://docs.unity3d.com/Manual/VRDevices-GoogleVR.html

Since Google VR works on phones, you need to set up either Android or iOS development, as described above. 

Google provides some additional instructions, which you might find useful (though you no longer need to download GoogleVR), both for Android:

https://developers.google.com/vr/unity/get-started

and iOS

https://developers.google.com/vr/unity/get-started-ios