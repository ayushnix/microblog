+++
title = "Use git archive To Create Releases"
[taxonomies]
tags = [ "git" ]
+++

I've been creating releases of one of my projects on GitHub like an idiot by manually copy-pasting
the folder and creating a `tar.gz` file. I was considering automating the entire thing using a
script but then I found `git archive`.

```
git archive --format=tar.gz -o tessen-1.2.3.tar.gz --prefix=tessen-1.2.3/ HEAD
```

Now I just have to automate creation of a SHA256 checksum file and sign it using GPG and signify.
