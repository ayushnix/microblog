+++
title = "Enterprise Business Class TP-Link EAP 225"
[taxonomies]
tags = [ "hardware", "AP"]
+++

I bought the [TP-Link EAP225 v3][1] access point a few years ago to extend my WiFi range. At the
time I bought this device, official OpenWrt support didn't exist for it. I recently noticed that
official support is available and I decided to flash OpenWrt on it. Before I could do that, I had to
SSH into the device.

I was greeted with a sight which has increased my skepticism and cynicism against software/hardware
which are targeted towards "enterprise" customers. The busybox version on the access point was
`1.20.2` and the Linux kernel version was `3.3.8`, both of which were released almost a decade ago
back in 2012. What's even more funny is that unlike usual consumer routers, this access point has
been receiving regular firmware updates, which helps build the illusion that TP-Link really does
care about the security of the device.

Are you using a router or an access point with its stock firmware?

[1]: https://www.tp-link.com/us/business-networking/ceiling-mount-access-point/eap225
