---
layout: post
title:  "PlexConnect"
date:   2013-08-24 13:00
categories: general
---

**UPDATE:** Well it was going to happen at some point, during the recent channel update on the ATV, Apple have stopped PlexConnect from working. Hopefully a solution will be found soon.

So a while ago I wrote [three posts][myMediaSetup] which explained my home media setup using XBMC on a jailbroken ATV2 and while I still think its a very good system, over the past month I've been playing around with an alternative.

I started having a problem with my ATV, constantly crashing and requiring a hard reset. Not really a problem, when it's happened in the past I've just put the ATV through a fresh jailbreak and away I go. However, the latest version of the Seas0npass is tethered only and I always try to avoid them if I can. So when I heard about Plexconnect I decided to give it a go; it is the brainchild of three brilliant individuals Baa, roidy and f00br and it allows you to access your Plex media library on your ATV *without* jailbreaking!

Plex is an off-shoot of the XBMC project and I have to say that I actually prefer the way it works, there are two separate components which make up Plex. The first is the [Plex Media Server][plexMediaServer] which allows you to add your media sources, enter your metadata and if you want actually playback your media all through the web interface. The advantage of this is that any computer on your network can access your library simply through a web browser. In fact i'm so impressed with it, i'm considering looking at using it at work in order to replace the custom/ media system we currently use. The second component is the [Plex Media Player][plexMediaServer] while this component isn't strictly necessary it does present a very nice navigation system for your media. In order to install Plex on your ATV2 you would have to jailbreak it, just as with XBMC, however it has not been updated to work with the latest ATV firmware.

This is where [PlexConnect][plexConnect] comes in, it is essentially a set of python scripts which creates a DNS server. This server has one primary job, which is to divert the traffic heading to trailers.apple.com to the PlexConnect scripts which are running on your computer. On your ATV, you need to change your network settings so that your DNS is pointing to your computers IP address. From that moment on, the Trailers app on your ATV2/3 will connect to your media library. The nice advantage of this is that everything uses the native ATV layout, it looks brilliant and is ridiculously fast.

All of the encoding required to playback the none native file types is handled by your computer which essentially means that your ATV is simply the viewer of your media. It's initial release, while perfectly usable did have a couple of small bugs but the latest version from their GitHub repository includes some really nice additions and is rock solid. My favourite function of Plex has to be 'On Deck' which carries out two different roles. It allows quick access to an episode or film, you maybe half way through watching, or it allows for quick access to the next episode in a series you are watching. Both of which can make things considerably easy for you.

By using PlexConnect, it does that I no longer have access to the Trailers channel, but the truth is that I can live without it and its a small price to pay. It also means that I can keep my ATV as intended by Apple and for those of you using a ATV 3 it allows you to stream all of your media.

It remains to be seen, whether Apple will find a way to stop PlexConnect working but for now its a great option that I highly recommend.

[myMediaSetup]: http://dalemmanning.me.uk/guides/2013/03/23/building-a-home-theatre-system-part-1/
[plexMediaServer]: http://www.plexapp.com/download/plex-media-center.php
[plexConnect]: https://github.com/iBaa/PlexConnect