--- 
wordpress_id: 13
title: .ds_store no more (on network shares at least!)
wordpress_url: http://elaptics.wordpress.com/2006/04/26/ds_store-no-more-on-network-shares-at-least/
layout: post
categories:
    - mac
    - terminal
---
Nothing exciting (for most people) but I've just finally found an easy way to stop creating the useless .ds_store files on non-mac network shares so I'm putting the info here for my posterity.

http://docs.info.apple.com/article.html?artnum=301711

1.  Open the Terminal
2.  Type:
    `defaults write com.apple.desktopservices DSDontWriteNetworkStores true`
3.  Press Return
4.  Restart the computer

As found on [http://www.textsnippets.com](www.textsnippets.com) (which also may come in handy in the future)
