---
layout: post
title: Objectives for October 2017
author: Mike Ray
excerpt: Setting out my development objectives for October 2017
tags: [project]
permalink: /blog/:title/
---

After a hiatus of a few months development is happening again.

Here are the immediate objectives as of the end of September 2017.

## F123 Pi

There are a number of things which absolutely *must* be done to progress with the [Raspberry Pi][rpi] version of F123. These are:

### Write a `speech-dispatcher` Audio Module for OMX

I need to write a `speech-dispatcher` module which interfaces to my OMX audio library.

This is because there is still the stuttering problem with text-to-speech on the Pi due to a broken (for tts) ALSA driver for the Broadcom GPU.

Without this we cannot:

* Use a desktop (graphical) with the Pi without using a USB audio dongle to provide audio.
* Use Emacspeak without either completion of my in-progress Emacspeak speech server or the `speech-dispatcher` module mentioned above.

2. Complete the `bootstrap` code which generates an F123Pi root filesystem on a running Pi.


## F123 x86_64

It is believed most, if not all of October will be occupied by Pi development.


[ala]: https://archlinuxarm.org/
[rpi]: https://www.raspberrypi.org/


