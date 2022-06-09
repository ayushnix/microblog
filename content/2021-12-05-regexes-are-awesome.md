+++
title = "Regexes Are Awesome"
[taxonomies]
tags = [ "regex" ]
+++

Let's say you download a useful bash script that uses bubblewrap to sandbox electron bloat like
Signal. The script is great but, unfortunately, it uses `function blah { }` to define functions
instead of `blah() { }`. There are 19 such "functions" in this script. You could manually change all
of them to the latter format. Or, you could use a regex in vim and change it in a few seconds.

```
:%s:^function \([[:alpha:]_]\+\) {:\1() {:g
```

`[[:alpha:]_]` matches an alphabet and the `_` character. The `\+` ensures to match multiple letters
of this pattern. The `^` at the beginning ensures that the line starts with `function`.

We've surrounded the pattern we wrote with `\(` and `\)` which is called "grouping". All we did is
"capture" that pattern because we'll need it later when we make the substitution we want. We didn't
capture `function` and ` {` because we want to remove them.

All that's left is to make the substitution with `\1`, our captured pattern, and `() {`.

Awesome.
