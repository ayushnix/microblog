+++
title = "The Problem With Dark Mode"
[taxonomies]
tags = [ "a11y" ]
+++

I've often felt that the WCAG 2.0 guidelines for colors don't make sense when choosing colors for
dark mode but I couldn't articulate my issues until I found a [twitter thread by Adam Wathan][1] a
few weeks ago. I discovered WCAG 3.0 APCA while creating the theme for this website and I assumed
that maybe APCA will finally solve the issue of terrible dark mode colors on websites. I was wrong.

I don't mean to disparage anyone but I was browsing [Wolfgang Müller's blog][2] looking for
inspiration to create my own blog. I tried reading one of the articles on his blog in dark mode but
couldn't continue after a few lines because of the uncomfortably high contrast. The white text
started causing halation in my eyes. Sure enough, `f0f0f0` as the text color and `000000` as the
background color passes both WCAG 2.0 and WCAG 3.0 APCA. I'm pretty comfortable with the OneDark
colors in my terminal so I've used them for the dark mode on this website as well. Unfortunately,
`abb2bf` as the text color and `282c34` as the background color fails WCAG 2.0 AAA and scores a 0
rating in WCAG 3.0 APCA, for body text at 18px font size with the font weight set to 400.

I don't mean to imply that my choice of colors is better for everyone compared to white text on a
black background but it is certainly better for me. At this point, either web browsers should
provide an easy switch to temporarily change the value of `prefers-color-scheme` for a specific
website or website owners should bite the bullet, use JavaScript, and provide a switch to let the
reader change `prefers-color-scheme` themselves. The best solution I've come across to solve this
issue is providing multiple theme options in a dropdown menu like [mdbook does][3], although this
option is probably reprehensible to some folks (_cough_ GNOME _cough_). No, using Dark Reader isn't
an option for me because of significant perfomance issues.

[1]: https://twitter.com/adamwathan/status/1304490267769221121
[2]: https://oriole.systems
[3]: https://rust-lang.github.io/mdBook/
