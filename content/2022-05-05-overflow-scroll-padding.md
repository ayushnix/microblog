+++
title = "Absent Right Padding In Firefox"
[taxonomies]
tags = [ "css" ]
+++

I'm not entirely sure why this is happening but if I use `overflow-x: auto;` for the `pre` and
`code` elements, Firefox ignores the padding on the right side of the `code` block if the content
inside `code` overflows horizontally. Chromium does not seem to have this issue.

I found [this discussion][1] on GitHub going all the way back to 2016.

[1]: https://github.com/w3c/csswg-drafts/issues/129
