+++
title = "Eliminate Layout Shift Due To Scrollbar"
[taxonomies]
tags = [ "css" ]
+++

I've noticed this issue before on many websites, including GitHub. If you have a web page open with
a scrollbar and go to another web page on the same website without a scrollbar, layout shift
happens. I think we can safely agree that layout shift is annoying as fuck and should never happen.
The popular solution to this fix this problem seems to be

``` css
html {
  overflow-y: scroll;
}
```

This will always show a scrollbar, even if it isn't required. There are some [hacks][1] with viewport
units as well. However, the "proper" solution to this issue is

``` css
html {
  scrollbar-gutter: stable both-edges;
}
```

Unsurprisingly, as of 2022-04-28, Safari [doesn't support this][2]. Oh well, `¯\_(ツ)_/¯`.

[1]: https://aykevl.nl/2014/09/fix-jumping-scrollbar
[2]: https://caniuse.com/?search=scrollbar-gutter
