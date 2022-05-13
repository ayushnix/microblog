+++
title = "Absence of Decent Terminal File Manager"
[taxonomies]
tags = [ "linux" ]
+++

I quit using GUI file managers on Linux ever since I found [ranger][1] more than 5 years ago.
However, ranger is written in Python and it's noticeably slower than alternatives like [lf][2],
which is what I've been using for the better part of the year. Unfortunately, using lf has become a
source of surprise and frustration due to [this bug][3]. This bug was noticeable in r26 but has made
lf unusable in r27. I don't know why but I got turned off looking at [joshuto][4]'s home page.
[nnn][5] has made some design decisions which I despise with a passion, heavy use of environment
variables being one of them.

I'll go ahead and use [xplr][6] for now but in my opinion, the lack of dual panes (or better yet,
miller columns) in a terminal file manager is a fundamental flaw. You end up wasting time going in
and out of directories and files you may not want to rather than glancing over their contents in a
preview pane. If there are no better ranger-like terminal file managers available in the near
future, I'll probably create my own.

[1]: https://github.com/ranger/ranger
[2]: https://github.com/gokcehan/lf
[3]: https://github.com/gokcehan/lf/issues/821
[4]: https://github.com/kamiyaa/joshuto
[5]: https://github.com/jarun/nnn
[6]: https://github.com/sayanarijit/xplr
