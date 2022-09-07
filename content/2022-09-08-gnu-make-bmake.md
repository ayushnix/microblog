+++
title = "GNU Make and bmake"
[taxonomies]
tags = [ "linux", "bsd" ]
+++

I was trying to create a Makefile for a personal project when I recalled that [bmake][1] exists, a
portable version of make from NetBSD. bmake seems quite similar to [OpenBSD's make][3] as well. I
was interested in making my Makefile portable and compatible with both GNU Make and bmake but I
quickly ran into a roadblock.

GNU Make uses `$^` as [an automatic variable][2] to expand into the list of all prerequisites
(sometimes called dependencies or sources) provided to a target but bmake uses `$>` to do the same
thing. Here's a simple Makefile.

<pre tabindex="0"><code>myfile: file1 file2
	cat file1 file2 > myfile</code></pre>

The second line of this Makefile can be rewritten as `cat $^ > $@` for GNU Make. However, it needs
to be written as `cat $> > $@` for bmake. `$@` is the name of the target, which is `myfile`.

It looks like I can either
- not use automatic variables and write all the sources manually
- or  write Makefiles to be either GNU Make compatible or bmake compatible

Am I missing something?

[1]: https://www.crufty.net/help/sjg/bmake.htm
[2]: https://www.gnu.org/software/make/manual/make.html#Automatic-Variables
[3]: https://man.openbsd.org/make
