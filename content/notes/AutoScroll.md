---
title: "Auto Scroll"
tags:
- Software
- Projects
enableToc: false
---

*I came up with this idea back in April. Since then, someone turned it into an actual device that [you can buy](https://giftcrawler.com/products/tik-click). Pretty neat.*

I've been wanting to be able to automatically scroll through TikToks, YouTube Shorts, etc. for a long time. My use case for this is that I get annoyed when I want to watch videos when I'm in the shower and my hands are wet. I know this is a terrible use case but I thought it would be fun to make this work.

I figured calling an API would be a bad idea since it would take too long to deploy and use on iOS, and I wanted to build something I could use soon. I went down the hardware route for 30 minutes before realizing I definitely don't have the hardware chops to pull that off. Instead, I started thinking a little more outside the box. Since TikTok is controlled by simple swipe motions, I figured Apple would have a good way to automate these controls. Shortcuts has some cool functionality to mimic this behavior, but I wanted to be able to use this hands-free.

I settled on voice control since it lets you perform a gesture upon a voice command (a great accessibility feature) and I was easily able to create commands to scroll up and down. I mapped the words "next" and "back" to their respective up- and down-swipes which worked surprisingly well. Hacking stuff together like this is a fun reminder that knowing how to program stretches beyond coding on a computer - many of our day-to-day problems can be tackled through programmatic approaches.

*Aside: I think [end-user programming](https://www.inkandswitch.com/end-user-programming/) should be *much* easier. A long term project I have in mind is some kind of software that lets you stitch APIs together - think [Zapier](https://zapier.com/) but on a much more personal level. I dream of being able to set reminders by sending an iMessage, setting up stock market monitoring via Slack in a few clicks, and much more. I've tinkered with Apple shortcuts for a while and have seen cool implementations like [delayed messages](http://caleb.software/posts/ios-delayed-messages.html) using Apple Calendar. However, this software isn't as robust and versatile as I'd like, and though Apple will get better at this with time I doubt they'll integrate with **all** the services I use (especially those owned by third parties).*