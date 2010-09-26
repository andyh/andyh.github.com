--- 
wordpress_id: 12
title: Easier editing of TypoScript
wordpress_url: http://elaptics.wordpress.com/2006/04/08/easier-editing-of-typoscript/
layout: post
categories:
    - textmate
    - typo3
---
I've recently discovered TextMate from [www.macromates.com](http://www.macromates.com) - a superb text editor, previously I've been using TextWrangler but I'm slowly using TextMate more and more, one of it's really great features is it's expandability through the use of bundles.

In getting to grips with the bundle editor I decided to put together a bundle for editing TypoScript so that it has syntax highlighting plus I've added some of the more common TypoScript objects as snippets to make it much quicker to put your typoscript together.  I've put a link to the TSRef doc online as well as ensuring the comment toggle puts the right comment symbol in.

Not sure how it measures up as a first attempt but [drop me a line](mailto:andy@elaptics.co.uk) if you find it useful or would like to see some other things added to it, likewise if you add any more features why not send them to me so I can include them here.  If enough people are finding it useful then we can also consider getting the bundle added to the main repository at macromates.

I've added the following scope selectors to the language grammars which you'll almost certainly want to add to your theme to have the syntax highlighted. (Whether these are the best scopes to use I don't know but feel free to suggest others).

    entity.other.tsobject
    entity.other.tsconstant
    entity.other.tsvalue
    entity.other.tscopy

**UPDATE:**

The bundle is much updated and now available from the macromates subversion repository.  Thanks to Sudara there is also a theme and a much better language grammar. You can find it under the Review directory. (Maybe one of these days I'll iron out all the kinks and get it into the main section)
