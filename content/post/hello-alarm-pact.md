---
title: "Hello Alarm Pact"
date: 2018-02-16
draft: false
tags: ["alarm pact", "react native", "connect iq"]
---

# Turn off that alarm!#

I've never really understood how couples do it. Surely they don't both wake up at the same time each morning? Does the early riser just wake up naturally, no shrieking alarm with ten snoozes to get them out of the bed, unintentionally (or maybe intentionally?) waking up their significant other at the same time? Wake up lights seem like all the rage, but that seems just as rude as a blaring noise -- like pulling open the curtains when your partner doesn't have to wake up for another hour or two! I'm guessing that the alarm habits of couples is an unspoken frustration -- it's obnoxious, but what choice is there?

Enter activity trackers with sleep tracking and silent alarms! Wear the tracker overnight and be gently awoken by vibrations on your wrist and a lovely graph telling you how poorly you slept! The nicest ones will even wake you when they sense your sleep is lightest -- refreshing! And unless your partner is an incredibly light sleeper, they are none the wiser that you are silently cursing at your tracker to let you sleep. One small problem, though... If you are anything like me, your body has figured out how to disable the alarm quickly, even in a half asleep daze. There goes your wakeup call.

Phone apps have started to fill the gap for those of us whose bodies outsmart our desire to be productive in the AM. They run the range from making you get up and do jumping jacks, stand on a mat in your bathroom, or scan a barcode (or series of barcodes) positioned throughout your house. Seems like a great idea to me, but I've always been horrified to try it. Odds are good I will just sleep through my alarm app, reminding me over and over again to scan that barcode in the bathroom, while my wife screams and struggles to figure out how to turn it off. In addition, the original wake up call is still a blaring alarm. Back to the original problem!

# Best of both worlds?#

Given this predicament, I had a thought the other day... What if my alarm and my activity tracker worked together? My activity tracker, serving as the little vibrating reminder to get myself in gear, with a corresponding app on my phone forcing me to do something to turn off the alarm on the activity tracker. This seems like the best of everything! My partner will continue to be none the wiser, with all alarms being silent, but no simple way to disable the alarm from my activity tracker -- take that half asleep body!

## Concept ##

It's summarized above, but here is the general idea:

1. Before going to bed at night, you plug in your phone and open up the companion app.
2. You crawl on bed, strap on your activity tracker (if it wasn't already on) and open up the app on tracker (obviously this will be limited to devices that support customs apps).
3. You set the alarm time on your tracker app, which sends it over to the companion app (as a backup). If you don't have the companion app open, you'll get a nice reminder to open it up!
4. You drift off to sleep.
5. Five AM rolls around and your companion app tells the tracker it's time to wake up! Go go vibrations!
6. Silently awoken, you hop out of bed and go to your phone. Once there, you do something to turn off the alarm (scan a barcode, shake it vigorously, do some jumping jacks -- whatever wakes you up).
7. The tracker stop vibrating. You close the tracker app and the companion app.
8. Congratulations, you made it out of bed without waking up your partner!

## But what if?..##

Of course, there are some things that could go wrong in the above plan, depending on what the tracker apps support.

| Problem                                                      | Solution                                                     |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| You turn off the tracker app when you wake up. Take that tracker! | The phone acts as an emergency backup. If the tracker app stops pinging it at the appropriate interval, it starts blaring an alarm (back to partner angry factor, but only in emergencies). |
| You forgot to charge your tracker and it dies.               | Same solution as above! The phone is the backup!             |
| The phone dies overnight, restarts, etc.                     | The tracker is a backup for the phone, as well! You'll still get your alarm, but not the safeguard of the phone. Hopefully this won't happen often! |

# Learning Experience#

Turns out I don't know how to do mobile development and I don't know how to do device development. But that sounds less like a problem and more like an opportunity! Here's the learning plan, as of right now:

- I have a Garmin Vivoactive, which supports the [Garmin Connect IQ Platform](https://developer.garmin.com/connect-iq/). This means learning a new language, called Monkey C, plus getting familiar with implementation on small devices. I also need to sort out some details about how Connect IQ apps work with standard functions. Ideally the device would still record sleep while the alarm app is working.
- [React Native](https://facebook.github.io/react-native/) seems to be all the rage when it comes to mobile development right now, and it seems sufficient given the mobile app should be fairly simple. Plus, I already know web development quite well. I will most likely be implementing it with [TypeScript](https://www.typescriptlang.org/), though, since I love me some types! I'm guessing I'll need to make use of [Native Modules](https://facebook.github.io/react-native/docs/native-modules-ios.html) to implement the Connect IQ APIs. The likely outcome will be a separate general use library for that integration.



So that's it! The next project in line and something that, unlike my "standing desk automation" app, I can likely actually achieve without devoting excessive amounts of time (that I do not have with a 7 month old at home).