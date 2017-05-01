---
layout: post
title: List Keybindings
excerpt: How to list keybindings for major modes in emacs
author: Rill
tags: [emacs, hints]
permalink: /blog/:title/
---

Working in a buffer and you don't know what keybindings are available?


1. Just type:

        c-h b
	
2. You receive the message:

        displaying keybindings in help window
	
3. Now type:

        c-x c-b
	
4. Scroll down the list of available buffers and find one that looks
    something like this:
	
        %  *Help*
	
5. Look for a line something like this:
	
        Major Mode Bindings:
	
6. You can use `c-x c-b` or `c-x <cursor left or right>` to get back to
   the list of buffers to find the one you were working in previously.

-------------------------------------------------------------------------------

Updated 2017/04/29 by Rill to include cursor movement with c-x.
