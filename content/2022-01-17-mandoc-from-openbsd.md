+++
title = "Use mandoc Instead Of man-db On Linux"
[taxonomies]
tags = [ "linux", "bsd" ]
+++

Although I discovered and switched to [mandoc][1] a few months ago, I've had a [tab][2] open in
Firefox for several months and I finally got around to reading it. I'm impressed by the amount of
work that was put into mandoc. I'm obsessed with reducing latency of the tools on my terminal and
mandoc is much more snappier than man-db, at least in my experience. If you live inside the terminal
for most of your tasks and read man pages, try using mandoc instead of man-db. If your distribution
doesn't package mandoc, you should use a different distribution.

I want to write man pages in mandoc too but, for now, [scdoc][3] is significantly more convenient to
use.

[1]: https://mandoc.bsd.lv/
[2]: https://www.bsdcan.org/2018/schedule/events/958.en.html
[3]: https://git.sr.ht/~sircmpwn/scdoc/
