---
layout: post
title: Text mode as Default Major Mode for Emacs
author: Mike Ray
excerpt: I have made text-mode the default major-mode in our emacs and emacspeak installations
tags: [emacs]
permalink: /blog/:title/
---


I have added code to `init.el` in the default `.emacs.d/` installation to make text-mode the default 
major-mode.

This means that text-mode will be the default major-mode rather than `fundamental-mode`.

I have also added code to turn on `auto-fill-mode` when `text-mode` is active. When writing long 
lines this will make the lines wrap at screen boundary.


