+++
title = "Markdown Is A Necessary Evil"
[taxonomies]
tags = [ "markdown", "orgmode" ]
+++

Markdown, no matter what the specification is, is a deceptively simple markup language to understand
and write documentation with. I've written my entire personal wiki using markdown because that's
what [mkdocs][1] uses. However, it's apparently a shitty markup language for anyone who wants to
parse it or develop a parser for it. [A blog post][2] by Eric Holscher and a [blog post on
undeadly][3] provide more details on why markdown is a shitty language for a developer. [Here's
another forum discussion][9] about possible ideas to reduce ambiguities in CommonMark. Perhaps this
is why the [treesitter parser for markdown][4] slows down neovim to a crawl to the point where
writing documentation is no longer fun. Oh, and this parser was merged after another markdown parser
[kept crashing neovim][5].

Alternatives? Unfortunately, I don't think there are any decent alternatives. A [blog post][6] by
Karl Voit convinced me about Org Mode being a reasonable markup language but, as expected, there's
no ecosystem for Org Mode outside Emacs. Maybe I can write articles in Org Mode but convert them
into markdown before using them? Maybe [neorg][7] or [orgmode.nvim][8] can work?

[1]: https://www.mkdocs.org/
[2]: https://ericholscher.com/blog/2016/mar/15/dont-use-markdown-for-technical-docs/
[3]: https://undeadly.org/cgi?action=article&sid=20170304230520
[4]: https://github.com/MDeiml/tree-sitter-markdown
[5]: https://github.com/nvim-treesitter/nvim-treesitter/issues/872
[6]: https://karl-voit.at/2017/09/23/orgmode-as-markup-only/
[7]: https://github.com/nvim-neorg/neorg
[8]: https://github.com/nvim-orgmode/orgmode
[9]: https://talk.commonmark.org/t/beyond-markdown/2787
