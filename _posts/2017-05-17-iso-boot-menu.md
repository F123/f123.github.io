---
layout: post
title: ISO Boot Menu Improvements
author: Mike Ray
excerpt: Improvements to audible feedback and menu options on the ISO boot process
tags: [iso]
permalink: /blog/:title/
---

I have made some improvements to the boot menu for the ISO installer.

I had managed to 'break' the audible bell on boot, which I have fixed now. This is a list of what I 
hve done:

* Put back the audible bell (beep)
* Removed network and http boot options from the menu
* Added a timeout to the menu which will boot the ISO when it expires

There are now three options on the menu:

1. Boot ISO
2. Reboot
3. Power off

Wording may change.

I am also going to replace the graphical menu with a purely text menu with no background and with 
high-contrast menu options for people with some vision.

The boot process is now:

1. Boot the ISO. When you hear the beep, pressing enter will immediately boot the ISO.
2. If you wait for the timeout to expire it will also boot the ISO.
3. When you hear the beep, pressing down arrow once and then enter will boot the installation 
	process again.
4. When you hear the beep, pressing down arrow twice and then enter will power-off the computer.

I haven't decided yet how long the timeout should be but think ten seconds is plenty.

