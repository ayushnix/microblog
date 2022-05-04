+++
title = "Building Custom OpenWrt Images"
[taxonomies]
tags = [ "openwrt" ]
+++

I've been using OpenWrt on my routers for several years at this point but one of the things that has
always bothered me is sysupgrades. A typical sysupgrade will always be a fresh installation and
although you can restore your packages and configuration, this isn't an automatic process.

I started creating a script to make sysupgrades less painful but then I discovered OpenWrt [image
builder][1]. There's also OpenWrt [buildroot][2], which is basically compiling the entire project
from scratch and the [SDK][3] which can be used to compile OpenWrt for a specific target.

The image builder should hopefully make OpenWrt sysupgrades pretty smooth. In my opinion, if you
install a few packages or make significant configuration changes on your OpenWrt installation, you
should probably create custom images using the image builder.

[1]: https://openwrt.org/docs/guide-user/additional-software/imagebuilder
[2]: https://openwrt.org/docs/techref/buildroot
[3]: https://openwrt.org/docs/guide-developer/toolchain/using_the_sdk
