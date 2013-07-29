---
layout: post
title:  "Building a home theatre system - Part 2"
date:   2013-04-01
categories: guides
---
Welcome to my second post looking at building a home theatre system. Sorry that this is being a little later than promised, I wanted to make sure everything was correct before I posted this. If you missed part 1 you can find it [here][dmmpart1]. This post will focus on the software required to jailbreak the ATV2.

As I mentioned during my first post, jailbreaking the ATV2 was an important move in building the home theatre setup I currently have. It turned my little hockey puck into a powerful media playback device and allow me to use XBMC, which is the centre of the entire setup. 

##### Jailbreaking - Installing

I use Seas0nPass from Firecore to jailbreak my ATV, I've never had any problems with it and its always been a very straightforward process. I would go into a complete step-by-step explanation of the process but the truth is the guys at Firecore are smart people and they can do a much better job than I can. You can find their instructions, as well the latest download links for Mac and Windows by  [clicking here] [spinst].

However there are a couple of things which could be useful to you, so here goes:  

- You will need a Micro USB cable in order to complete the process, most people do have at least one lying around the house but if you can easily pick one up from amazon.

- There are two types of jailbreak:  
	- _Tethered:_ A tethered jailbreak means that should you ever need to boot your ATV2 backup you will need to use Seas0nPass to bring it back to life (as a general rule any major iOS upgrade will result in a tethered jailbreak being available first).
	- _Untethered:_ My preferred type of jailbreak, once you have this installed you can shutdown/power up your ATV to your hearts content without the need to run Seas0nPass again.  
- Apple stop signing all previous versions of their ATV updates as soon as a new one is released, which means you need to be careful when beginning the jailbreak process. You can find the current jailbreak status of the iOS upgrades by [clicking here][spinstver].  	
	
##### Jailbreaking - Upgrading

So what about upgrading your jailbreak when a nice new iOS upgrade comes along ... Well this is where things get a little tricky, the first thing you need to consider is that it will generally take a little while for a jailbreak to be released for the newest upgrades. Apple aren't exactly keen on people changing the default settings of any of their devices and as a result they have a habit of throwing a few curveballs into the mix (See the ATV3 for an example).

Once a new jailbreak is available you will need to backup your important settings, especially if you do plan to use XBMC, as a new jailbreak will wipe your ATV. Luckily this isn't so difficult and you can SFTP into your device and copy your settings folder. I make use of [Forklift][forklift] in order to backup my settings but you can use just about any FTP software.

>  
> Example of backup procedure:  
>
> 1. Look up your ATV IP address :: Settings > General > Network  
> 2. Load Forklift or FTP software of choice.  
> 3. Create a new SFTP connection to the IP address of your ATV.  
> 4. Enter username: _root_ and password: _alpine_ (which is the default).  
> 
> From here you will have access to the root folder of the ATV and you can find the settings you want to > backup. For example the settings for XBMC can be found at:  
>
> _/private/var/mobile/Library/Preferences/XBMC/_ :: which contains all of your add-ons, skins and user data.  
> _/private/var/mobile/Library/Preferences/XBMC/userdata/_ :: which is just your user data and is the most important folder of all.  
>

I tend to create a backup of my user data folder every couple of weeks, so all I have to do after an iOS upgrade is copy the user data folder back and I'm good to go!


##### XBMC - Installing

There are a couple of different ways to install the latest version of XBMC _'Frodo'_, I tend to stick with the recommended install method which is to use the command line instructions. However if playing around on the command line isn't for you, you can purchase Firecore's [ATV Flash Black][firecoreatvflash] which will do everything for you.

XBMC themselves recommend the command line method and to be honest it isn't to difficult, just like Firecore they have a very comprehensive set of instructions [available here][xbmcinstall].

##### XBMC - Updating

The nice thing about XBMC is that you can update it all you want and your user data remains completely intact! Its always advisable to update to the latest version when possible as they are constantly ironing out bugs (if you are really brave you can switchover to using their nightly builds...).

Just as with installing XBMC, updating is very straightforward and the instructions are [available here][xbmcupdate]. While I've never had anything go wrong during the update, just remember to backup your settings every now and then.

##### XMBC - Add-ons

The greatest advantage that XBMC has is the number of add-ons which are available to you both official and unofficial. This includes additional skins (I've tried a fair few but I always comeback to the default which is extremely responsive on the ATV2), video plugins for services such as iPlayer or 4od and audio plugins for services such as Rdio or Spotify.

*****

So that's part 2 finished, thanks again for taking the time to read this. Next time I will discuss the software I use for the actual conversion of my media. Check back next week for part 3 and if you like what I've written, please let me know via twitter or the comments below.

[spinst]: http://support.firecore.com/entries/387605-jailbreaking-101-seas0npass  
[spinstver]: http://forum.firecore.com/topic/3418  
[forklift]: http://www.binarynights.com  
[xbmcinstall]: http://wiki.xbmc.org/index.php?title=HOW-TO:Install_XBMC_on_Apple_TV_2#ATV_5.x  
[xbmcupdate]: http://wiki.xbmc.org/index.php?title=HOW-TO:Install_XBMC_on_Apple_TV_2#Updating  
[firecoreatvflash]: http://firecore.com/atvflash-black  
[dmmpart1]: http://dalemmanning.wordpress.com/2013/03/23/building-a-home-theatre-system-part-1/

