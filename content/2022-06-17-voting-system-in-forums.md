+++
title = "Voting on Internet Forums Considered Harmful"
[taxonomies]
tags = [ "forum", "posse" ]
+++

Reply to [Better vote-enabled forums][1] by [Seirdy][2] and [On votes, and Indieweb forums][3] by
[Florian Maury][4]

I don't consider voting systems on online forums to be an effective tool to promote meaningful
discussions. A voting system assumes that collective populations of humans are capable of objective
judgement which would ultimately outweigh judgement clouded by prejudice. Nobody is free from
prejudice and I would include myself in that categorization. This inherent prejudice leads to the
formation of filter bubbles where prevailing popular opinions are made more popular and unpopular
opinions are made obscure. Florian has expressed similar ideas in [this post on lemmy.ml][5]

{% quote(author="Florian Maury (@X_Cli@lemmy.ml)", citeurl="https://lemmy.ml/post/307399") %}
Yet, from what I observe, the tool is mostly used for communities to self-administer filter bubble.
Some communities seem to behave like a hive mind, massively upvoting or downvoting until either the
dissident is assimilated in a very Borg way, or excommunicated.
{% end %}

I don't remember if I read about this somewhere or if it's an original thought but it's been on my
mind for quite some time now. I think voting systems should be completely removed, including upvotes
and downvotes. The typical sorting methods on Lemmy and on Reddit — Hot, Top, New, Old — should be
removed as well. These flawed methods should be replaced by randomized sorting of both posts and
comments on a post on each page reload for each individual user.

When it comes to post discovery, forum admins can decide the duration that a post is visible on the
first page containing `n` number of posts. Until that duration expires, the order of the posts
should be randomly sorted for each individual on each page reload. When it comes to comments, each
top level comment, while maintaining the level of its direct child comments, should be randomly
sorted on each page reload. The order of the 2nd level child comments, while maintaining the level
of their own child comments, should be randomly sorted as well. If this is confusing to understand,
I can summarize by saying that the structure and the level of comment trees should be preserved but
their order should be randomized.

This will ensure that popular opinions don't appear at the top of the page and unpopular opinions
aren't made obscure. It also incentivizes people to actively seek out quality comments rather than
just skimming the top level comments. What about posts and comments that are spam, low quality, or
just low effort? The flagging system should be retained and anyone can flag a post or a comment
provided a reason is mentioned. Of course, to prevent unnecessary flagging, the username should be
sent to the forum admins so that they can judge if the flag was legitimate and appropriate.

[1]: https://seirdy.one/notes/2022/06/14/better-vote-enabled-forums/
[2]: https://seirdy.one
[3]: https://broken-by-design.fr/notes/votes/
[4]: https://broken-by-design.fr
[5]: https://lemmy.ml/post/307399
