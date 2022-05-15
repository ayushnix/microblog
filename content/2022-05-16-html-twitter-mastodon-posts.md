+++
title = "Generating HTML-only Twitter and Mastodon Posts"
[taxonomies]
tags = [ "api", "shell" ]
+++

There's this thing called oEmbed which advises using iframes to embed content posts. The problem is
that on a static website such as this, iframes seem like an abomination. I wanted to retrieve a
tweet or a toot in its HTML form and add it to my post.

A few hours of reading API docs of Twitter and Mastodon and writing messy [shell script code][1] and
here's the result

<blockquote class="twitter-tweet">
<p dir="ltr" lang="en">"Aha! This is exactly what I was talking about!"
<br>

<br>

(Article has nothing to do with what he was talking about)
<br>

<br>

Remember folks, random clickbait YouTubers are not a reliable source of technology information. <a href="https://t.co/wThF0VdrFt">https://t.co/wThF0VdrFt</a>
</p>
— Hector Martin (@marcan42) <a href="https://twitter.com/marcan42/status/1525351488373297152">May 14, 2022</a>
</blockquote>

Here's a toot from mastodon

<blockquote class="mastodon-toot">
<p>Work-in-progress book on Linux kernel internals by 0xAX <a href="https://github.com/0xAX/linux-insides/blob/master/SUMMARY.md" rel="nofollow noopener noreferrer" target="_blank"><span class="invisible">https://</span><span class="ellipsis">github.com/0xAX/linux-insides/</span><span class="invisible">blob/master/SUMMARY.md</span></a><br><a href="https://fosstodon.org/tags/linux" class="mention hashtag" rel="nofollow noopener noreferrer" target="_blank">#<span>linux</span></a> <a href="https://fosstodon.org/tags/kernel" class="mention hashtag" rel="nofollow noopener noreferrer" target="_blank">#<span>kernel</span></a> <a href="https://fosstodon.org/tags/linuxkernel" class="mention hashtag" rel="nofollow noopener noreferrer" target="_blank">#<span>linuxkernel</span></a></p>
- BayLibre (@baylibre) <a href="https://social.treehouse.systems/web/@baylibre@fosstodon.org/108307448501709873">May 16, 2022</a>
</blockquote>

Oh, the script also helps crosspost this post to Mastodon. Maybe I'll add the Twitter and Mastodon icons near the blockquote to showcase the embeds.

All that's left is to somehow add a 'discuss on mastodon' link which points to the crossposted
mastodon toot although I'm not sure if that's possible because of the context limitations of Tera
templating engine.

[1]: https://github.com/ayushnix/microblog/blob/master/twoot
