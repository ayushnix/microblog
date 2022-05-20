+++
title = "Improving Sway PKGBUILD For Arch Linux"
[taxonomies]
tags = [ "linux" ]
+++

The PKGBUILD file for the sway wayland compositor on Arch Linux had a hard dependency on polkit
which didn't really make sense because sway doesn't depend on polkit. However, systemd does depend
on polkit to provide access to seat hardware devices and the user session to sway. The alternative
is using [seatd][1], a lightweight seat and session management daemon that can act as a replacement
of systemd-logind for this specific task.

I raised a [bug report][2] on the Arch Linux bugtracker and Brett Cornwall made [several
improvements][3] to the sway PKGBUILD since sway 1:1.7-2 was released. I also [updated the Arch
Linux wiki][4] to highlight these changes.

If you're using Arch Linux and sway, you can now uninstall polkit and use seatd which should already
be installed.

[1]: https://git.sr.ht/~kennylevinsen/seatd
[2]: https://bugs.archlinux.org/task/73547
[3]: https://github.com/archlinux/svntogit-community/commits/packages/sway/trunk
[4]: https://wiki.archlinux.org/title/Sway#Starting
