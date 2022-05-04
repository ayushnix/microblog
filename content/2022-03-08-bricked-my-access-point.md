+++
title = "Bricked TP-Link EAP225 v3 WiFi Access Point"
[taxonomies]
tags = [ "openwrt" ]
+++

While trying to make OpenWrt sysupgrades easier, I started experimenting with the OpenWrt
imagebuilder program, which is really just a bunch of scripts and a giant Makefile. Unfortunately,
my AP didn't boot properly after I flashed a custom image on it. I tried to go into failsafe mode
but encountered [this bug][1]. Turns out, the bootloader of my EAP225 doesn't have a HTTP server or
a TFTP recovery mode, unlike EAP245. I realized that my AP is soft-bricked.

My older self would have complained about this but I've realized that the OpenBSD motto of "shut up
and hack" applies when you're using open source software in a way that mere mortals aren't supposed
to. Looks like I may need to learn how to solder and use the serial console to install OpenWrt.

[1]: https://github.com/openwrt/packages/issues/17833
