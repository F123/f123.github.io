---
layout: post
title: Problems with the Arch Linux ARM Raspberry Pi root filesystem archives from archlinuxarm.org
author: Mike Ray
excerpt: Solving some persistent problems with Raspberry Pi root filesystem archives available from archlinuxarm.org
tags: [arch]
permalink: /blog/:title/
---

For some time I have been having a problem extracting the contents of
root filesystem archives for the [`Raspberry Pi`][rpi] downloaded from
[archlinuxarm.org][ala].

It needs `bsdtar` to extract files from the archives, GNU tar will not
do the job.

The problems I was having, it now seems, were due to the version of
`bsdtar` I was using, on a [`Debian`][debian] machine, was not
sufficient.

It is necessary to use a version of 3.3 or later.

When I installed the latest version on my `Debian` machine the problems extracting the files was solved.

But, there are more problems, read on.

There are three different archives available from the Web site:

* armv6h - For the original Pi models A and B, and B+.
* armv7h - For the Pi 2.
* armv8h - For the Pi3.

Only the first will work correctly on the original Pi, the first two
will work on a Pi2, and all three will work on a Pi3, as far as I know.

I have created `.img` files for all three architectures. I intend to
use the `armv7h` images for F123, as it is likely that the highest
number of users will have a Pi2 and not a 3, and anyway, with the
amount of memory on a Pi being well below the maximum for a 32-bit
system, there is little advantage to using a `armv8h` (64-bit) image.

As I mentioned above, I have created images for all three
architectures. But I have had problems getting an `armv7h` image to
boot.

I have followed all instructions to the letter for getting the archive,
extracting it and writing it to an image file and writing that image
file to an SD card, but it fails to boot.

So...what did I do next.

In order to get around this I have written a set of scripts, which,
when run on a running Pi2, will `bootstrap` a new archive containing
all packages that were installed on the host Pi, and do all the other stuff needed to turn this collection of files into a bootable image file when writen to an SD card.

This involves the following (not exhaustive) list of things to do:


1. Grab a list of what packages are installed on the host.
2. `pacstrap` a new `chroot` in a sub-directory.
3. `arch-chroot` to this directory.
4. Enable `sshd` and `dhcpcd` services.
5. Set the root password.
6. Set the host name.
7. Create the first ordinary user and set the password.

There may be other steps which develop which are not included in this list.

For completeness, here is a list of three links from which to download filesystem archives from archlinuxarm.org:

* [Original Pi, models A and B, and B+][armv6h]
* [Pi2 all  models][armv7h]
* [Pi3, 64-bit Pi, all models][armv8h]



It is now my intention to use this `bootstrap` system to create the
`F123pi` images as they develop.

Not relying upon the regular creation of a filesystem image on the
archlinuxarm.org Web site is better anyway, I think.


[rpi]: https://www.raspberrypi.org/
[ala]: https://archlinuxarm.org/

[armv6h]:http://archlinuxarm.org/os/ArchLinuxARM-rpi-latest.tar.gz
[armv7h]: http://archlinuxarm.org/os/ArchLinuxARM-rpi-2-latest.tar.gz
[armv8h]: http://archlinuxarm.org/os/ArchLinuxARM-rpi-3-latest.tar.gz



[debian]: https://www.debian.org/
