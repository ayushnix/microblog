+++
title = "Successful Recovery of EAP225"
[taxonomies]
tags = [ "hardware", "openwrt" ]
+++

I tried to solder the pads and the resistors in the EAP225 myself but things didn't work out as
expected. A friend suggested that I should get the soldering done from a local electronics repair
shop. I had almost given up on recovering my access point but the guy in the repair shop I visited
finished soldering pretty quickly. I installed [picocom][1], gained access inside my router,
uploaded a vanilla sysupgrade image using the HTTP server built into python, and flashed it.
`PaulFertser` from the `#openwrt` IRC channel on OFTC helped me out a lot during this process.
Thanks Paul!

Will I build custom images for my OpenWrt devices after this experience? I probably won't mess
around with custom images if the device in question doesn't provide easy access to the serial
console or doesn't have a recovery mode like the EAP225. However, the original problem that got me
started down this path is still present. Yeah, `sysupgrade` is still painful.

[1]: https://github.com/npat-efault/picocom
