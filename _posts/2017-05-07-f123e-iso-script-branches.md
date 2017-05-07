---
layout: post
title: Branches on f123-iso-script
author: Mike Ray
excerpt: Working branches in the f123e-iso-script repository
tags: [ISO]
permalink: /blog/:title/
---

In the `f123e-iso-script` repository I currently have two working branches:

* master
* alpha_iso

The `master` branch has everything which can be regarded as the _base_ work in configuring the 
build of an Arch Linux based F123e .iso file.

The `alpha_iso` branch can be regarded as my local working branch while I work to release early 
versions of the .iso file.

I expect to also have a `beta_iso` branch at some point when the work moves from the _alpha_ phase 
into the _beta_ phase.

I have pushed the `alpha_iso` branch to the remote server, but currently the differences between 
this and `master` are minimal and relate to the naming of the file.

As I work to add things to the `alpha_iso` branch is will eventually merge with `beta_iso` and then 
ultimately back into `master`.



