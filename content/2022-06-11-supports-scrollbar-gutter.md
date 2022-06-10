+++
title = "Eliminate Layout Shift Due To Scrollbar - Part 2"
[taxonomies]
tags = [ "css" ]
+++

I wrote about [using `scrollbar-gutter`][1] to eliminate layout shift when browsing across pages
that may or may not need a vertical scrollbar. I was, however, avoiding using it because [Safari
doesn't support it][2] yet. Well, that's not necessary anymore because today I learned about
`@supports` in CSS. Here's a piece of code that should probably be part of all popular CSS
reset/normalize projects.

```css
html {
  overflow-y: scroll;
}

@supports (scrollbar-gutter: stable both-edges) {
  html {
    overflow-y: auto;
    scrollbar-gutter: stable both-edges;
  }
}
```

If you don't care about symmetry, you can remove `both-edges`.

[1]: /scrollbar-layout-shift
[2]: https://caniuse.com/mdn-css_properties_scrollbar-gutter
