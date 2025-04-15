---
title: "Google & It's Hypocrisy in Messaging"
date: 2025-02-15
author: "Christian Thackston"
---

## Introduction

I'd like to preface this by saying that while I do own many Apple products, I am not a "fanboy" nor a "hater" of anyone's products. I have, over the years, daily driven both Android and Apple devices on mobile, as well as MacOS, Windows, and Linux on the desktop/laptop. I am a huge proponent of open standards. I will never use email that doesn't support IMAP/SMTP, for example. I believe users having the freedom of choice to use any product/service they wish while being able to interact with those who chose differently is essential if we want communication to remain open and simple.

## The State of Mobile Messaging

There are certain things that cannot be easily federated, however. Things like messaging apps are something that are extremely annoying, especially in America, where there isn't a "de facto" messaging app like QQ in China or Line in Japan. 

Messaging via phone number is typically the default here, and that is where SMS comes in. Being around for around 20 years at this point, it really needs no introduction, but its shortcomings have been increasingly apparent over the last few years. No read receipts, very limited image sending, abysmal video sending, and carrier limits are among some of the biggest issues I've had over the years, along with its awful security. 

Apple introduced iMessage to combat this. Creating unlimited free messaging that vastly improves the experience over SMS, both in security and usefulness. It's a fantastic service but is, unfortunately, locked to Apple products. That left Android users with a few options: Try and make your friends switch to a third-party app, deal with it, or [buy your mom an iPhone](https://9to5mac.com/2022/09/07/tim-cook-explains-why-apple-refuses-to-adopt-rcs-buy-your-mom-an-iphone/).

## The Rise of RCS

All of these solutions are awful, and for something as simple as communication, it should not be a factor end users should ever even have to think about. In the last few years, the GSMA, led by Google in large part, tried to put a stop to this problem by creating Rich Communication Services (RCS). This was a godsend for Android-to-Android communication since until then, Android users were stuck using SMS unless they wanted to use a third-party app. It also largely solves the issues with SMS (sans E2EE, which I'll get more into later), but was created in the open and was designed to be interoperable between devices and platforms. This is where my issues with RCS and Google begin.

## Google's False Promises

While RCS is, on paper, "open," it is anything but. It is tied to Google Play Services and the Google Messages app, which on its own forces vendor lock-in as no public API nor third-party apps implement the standard on Android. Additionally, while the standard is carrier agnostic, Google has elected to instead force most users to instead go through its own Jibe backend instead, further increasing vendor lock-in. The cherry on top of all of this is that Google decided to develop and implement a completely proprietary and undocumented E2EE spec into exclusively, again, the Google Messages app.

Google decided to continue to campaign this as an "open standard" while continuing to lock it to its own proprietary app, and more importantly, to Play Services, refusing to implement any RCS functionality into AOSP directly. While AOSP has been a "look but don't touch" kind of open for years now, this was a new low for Google, while they continued to campaign on being the hero to fix communication with their whole "Get the Message" campaign.

Apple did finally implement RCS in iOS 18 (due to EU regulations), and that is indeed a good thing, and as I've recently switched back over to iOS, this issue no longer affects me directly. It did affect me, however, when I was using GrapheneOS on my Pixel 9. The hoops that I had to jump through to enable RCS were absurd for an "open standard," and while there is nothing technically stopping anyone from implementing their own, open source version of RCS and it being used in alternative Android distributions, the barrier to entry is very high, and Google will continue to monopolize Android until AOSP becomes nothing more than what Darwin is to Apple: completely useless on its own.

## The Future of Messaging

I think the thing that upset me most about this whole thing, however, is how Google has used this as advertising about how much more "open" they are compared to Apple while they continue to push what is effectively their own undocumented extensions to the protocol (Apple's implementation of RCS also doesn't include E2EE as it's not formalized in any way). I hope that someday a truly open protocol comes along, but that seems exceedingly unlikely at this point, and as mobile communication becomes more essential, I think fragmentation will only continue to grow.