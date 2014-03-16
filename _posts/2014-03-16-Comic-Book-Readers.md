---
layout: post
title: Comic Book Reading Apps
date: 2014-03-16 08:23:54
category: comics
---

Alongside my recent move to purchasing digital comics, came the need to select a comic book reading app for my iPad. Ideally I was looking for an app which would allow me to read my comic book files straight from my synology NAS without the need to sync them onto my iPad unless I wanted to. It took a while but I eventually found [ComicGlass][ComicGlass] and it does everything I needed it to.

ComicGlass will allow you to copy comic books via iTunes or Dropbox but it also allows you to run your very own comic book media server. The developer has created versions of the [media server][CGMediaServer] for Windows and OS X, as well as PHP version which can be run on a web server. As the synology has the ability to run a web server with virtual hosts, I decided to go with the PHP version. The advantage of this is that my mac does not need to be running to allow me access to my comic books.

The setup is very straightforward, I created a new folder called 'ComicGlass' inside the web folder on the synology and copied the index.php file into it. The purpose of this php file is to create a index of the folders and files, ready to be served to the 'ComicGlass' app. Inside the ComicGlass folder, I've created another folder simply called 'comics' and all of my comic book files are saved into it.

Using ComicGlass I can quickly navigate my comic book collection and read them straight from the Media Server, providing they are cbz files. If you have cbr files it will download them before you can read them. It's a really nicely implemented system and the developer has clearly put a lot of work into it, however there a few small things that I hope get improved over time. The biggest one is the interface design, if you do want to download a comic it gets placed onto a wooden book shelf and unfortunately it just looks wrong on iOS 7. In reality it is a small thing but it is enough to disrupt the overall experience for me.

So over the past few weeks, I've been trying out [Chunky Comic Reader][ChunkyReader] and I've really been enjoying it. While I can't read straight from my NAS, it does allow me to access my comic folder via AFP and download them. The nicest aspect of the app is that it organises everything for you, just download the issues you want to read and Chunky will place them into the appropriately named categories. It also allows you to connect to all of the main cloud storage providers such as Dropbox, Google, Onedrive and Box, as well as supporting the Transporter sync protocol. It even supports connecting straight to your Image comics account, which is described as experimental but has worked pretty well for me so far.

I'm pretty sure that I'm going to stick with Chunky Reader for now, it's a really nice app that just makes the reading experience a pleasant one but I'm sure that I'll use ComicGlass from time to time as well. I'm really looking forward to seeing where the developers of both apps take them next.

[ComicGlass]: https://itunes.apple.com/gb/app/comicglass-comicreader/id363992049?mt=8
[ChunkyReader]: https://itunes.apple.com/gb/app/chunky-comic-reader/id663567628?mt=8
[CGMediaServer]: http://comicglass.net/download/toolsdownload/

