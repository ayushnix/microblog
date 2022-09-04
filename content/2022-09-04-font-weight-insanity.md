+++
title = "Don't Use Font Weight Less Than 400"
[taxonomies]
tags = [ "css" ]
+++

As I'm working on a CSS side project which has ended up taking more of my time than I would've
liked, I frequently come across blogs where website authors use `font-weight` values less than 400
on some HTML elements.

I don't claim to be an expert myself but maybe a blog post that talks about accessibility shouldn't
assume that a user will definitely download a web font that makes headings look fine at a font
weight of 100, which is extremely unusual, to say the least?

<figure>
  <img height="337" width="494" decoding="async" alt="an image that should h2 HTML element with a font-weight of 100" src="images/font-weight.jpg">
  <figcaption><p><code>&lt;h2&gt;</code> element with a <code>font-weight</code> of 100</p></figcaption>
</figure>

I mean, the value of `font-family` should have a fallback value like `sans-serif` for a reason — to
use system fonts in case web fonts are not loaded. Even if a user doesn't block web fonts like I do,
[Flash of Unstyled Text][1] (<abbr title="Flash of Unstyled Text">FOUT</abbr>) is a possibility that
should be considered when using web fonts, assuming the website author has chosen not to completely
hide text until a web font loads, which sounds worse. If FOUT happens, unstyled text should, at the
very least, be reasonably similar to the web font in question. I don't think any system font is
going to look usable at a `font-weight` value of 100.

Please stop using `font-weight` lesser than 400 on your websites, unless there's an excellent
reason.

[1]: https://web.dev/webfonts-quick/#dealing-with-fout
