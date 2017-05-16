---
layout: post
title: Inserting a page-break into an Emacs Buffer
author: Mike Ray
excerpt:How to insert a page-break (form-feed) into an emacs buffer
tags: [emacs]
permalink: /blog/:title/
---


I've seen page-break characters in files written with emacs, and when displayed in an emacs buffer they appear as a caret and a capital L, or at least they are spoken as 'caret L'.

But in reality they are just one character, and that is the ASCII 12 character, which is a page-break, also known as a form-feed.

It is commonly used to make text files more presentable when printed by making the printer eject the page and start on another.

This is not of much use to us as blind users but makes printed matter better for sighted people to read.

To insert a page-break into an emacs buffer, press:

	C-q C-l

