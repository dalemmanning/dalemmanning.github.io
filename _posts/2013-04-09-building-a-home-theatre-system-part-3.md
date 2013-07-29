---
layout: post
title:  "Building a home theatre system - Part 3"
date:   2013-04-09 15:11
categories: guides
---
Welcome to my third post looking at building a home theatre system. If you missed part 1 you can find it [here][dmmpart1] and part 2 can be found [here][dmmpart1]. This post will focus on the software actually needed to convert your media.

OK, so far I have discussed the various pieces of hardware which I use in order to playback my media and how to go about actually jailbreaking your ATV 2 and installing XBMC. This final part will take a look at the process I go through in order to actually convert my DVD's to individual media files.

My core software setup:

* DVD Ripping software :: [Mac DVD Ripper Pro][mdrplink]  
* Conversion software :: [Handbrake][handbrakelink]  
* Utility :: [Wimoweh][wimowehlink]

My workflow in a nutshell:

1. Rip the contents of each DVD to the Hard Drive (e.g. each DVD of a TV series).  
2. Load DVD Player and open the first DVD image.  
3. Use DVD player to identify the title numbers for each episode.  
4. Load Handbrake and add each title to the conversion queue, with each episode/film saving to my NAS drive and following a XBMC friendly naming convention.  
5. Hit Start and let it get on with it!

  
##### Step 1 :: Rip the contents of each DVD to the Hard Drive

So why rip the DVD's first when Handbrake is perfectly capable of converting straight from the DVD? The first answer is that I've found it provides better results and a faster conversion time overall. The second answer is because it allows me to create a batch conversion list within Handbrake which can be left to do its own thing without the need for intervention on my part. I tend to feed in the DVD's while working on other things, so its not like I'm sitting around waiting for each DVD to rip. I save the DVD image to my 'Shared' folder, although you can obviously save it anywhere you like. I've selected this folder because its the one folder which is excluded from my Time Machine backup!

For a while I ran [RipIt][ripitlink], but over the past 18 months I've switched over to [Mac DVD Ripper Pro][mdrplink] which has given me consistently reliable results. Really you can use the software of your choice here and both companies will allow you to try them out before you buy.

The latest versions of the both pieces of the software mentioned above will allow you to instantly convert the DVD if you wish, I've never tried using this function as I've always been happy with Handbrake but it certainly provides an easier option if you don't want to play around with different pieces of software.

_Just as a small side note, Blu Ray discs are a very different kettle of fish and I'll probably write about those in a later post._

##### Step 2 & 3 :: Use DVD Player to identify the title numbers for each episode

OK so this is possible the most tedious part of the whole process but a necessary one. Each DVD from a TV series will typically have 3-4 episodes on it and each of this episodes will live in a particular title. It is these title numbers which allow you to name your episodes correctly when you are setting up your queue in Handbrake during step 4.

This is what you need to do in order to identify the title numbers:  
  
1. Load DVD Player (If it runs in full screen, press escape).  
2. Click on File > Open DVD Media and click on the first image file/folder you want to open.  
3. Once you reach the menu, load the first episode and let it start playing.  
4. You will see that the Controller has the playback time currently displayed, click on the time twice. This will display the title number for you e.g. 14/51.  
5. Make a note of the title number and return to the main menu.  
6. Repeat the process until you have identified all of the episodes.

Now as a general rule, the title numbers will actually be fairly logical e.g. Titles 1 to 4 and once you have identified the pattern on the first couple of DVD's you can easily apply it to the rest of the series.

##### Step 4 :: Load Handbrake and add each title to the conversion queue.

My conversion software of choice is [Handbrake][handbrakelink], an excellent piece of open-source software which provides you with a range of built-in presets for almost all of the common apple devices such as the ATV 1-3, iPod, iPhone and iPad. Alternatively you can create your own presets which is what I've done.

You will need to play around with the presets until you have settings that you are happy with, you will probably find that the ATV options will do the job for you or at the very least provide a good starting point.

This is what you need to do in order to create your queue:  
  
1. Load Handbrake.  
2. When prompted to select a source, open the first image file/folder you wish to convert.  
3. Handbrake will then scan through the available titles, this can take a minute or so.  
4. Select the preset you wish to use (if you select and preset click on the cog button you can make it the default).  
5. Select the destination you wish to use to store your converted files.  
6. Select the title you want to convert (see step 2 & 3).  
7. Enter the name for the file (See the next section for a discussion of naming conventions).  
8. Click on the _'Add to Queue'_ button.  
9. Repeat steps 6 & 7 for each title on the DVD.  
10. Click on the _'Source'_ button to select the next image file/folder you wish to convert.  
11. Repeat the process for each DVD.  
12. Click start.  

Trust me I say that after going through it a few times this will become second nature to you! 

There are a couple of things to consider before you start using Handbrake:  

* The last stable release (0.9.8) has some bugs regarding Mountain Lion particularly if your machine is set to sleep after a period of inactivity. Handbrake isn't recognised by the system as being busy and as a result will put the whole system to sleep (a rather annoying problem when you are trying to convert a bunch of video!). This is where the excellent [Wimoweh][wimowehlink] app comes in, it allows you prevent system sleep if certain apps are running.
* You can also set the behaviour of Handbrake once it has finished the queue, simply go to _Handbrake > Preferences_ and in the _'When Done'_ combo box select an action. I've setup mine to shut down my machine once it has finished the current queue, but you can just tell it to display an alert window or even do nothing at all.

##### XBMC Friendly naming conventions

If you want XBMC to be able to scrap your files for you and download all of the required metadata so that you can get TV/Film information, you need to make sure that you name your files correctly. This will require a little bit of research on your part but its worth it. The two best resources you have at your disposal are [The Movie Database][mvdblink] and [The TV Database][tvdblink], you can find all of the required information on these two sites.

To give you an example of why some research might be required, lets take Doctor Who. Now I have a couple of seasons of the new Doctor Who starring Matt Smith that I wanted to add to my library, but it turns out that if I had just named the root folder _'Doctor Who'_ my episodes would have the information for the episodes starring Patrick Troughton! Instead I needed to name my root folder _'Doctor Who (2005)'_.

So once you have the correct name for you root folder you can start to build up everything else, in the end my Doctor Who folder looked like this:

* Doctor Who (2005)
	* Season 5
		* Doctor Who (2005) - S05E01
		* Doctor Who (2005) - S05E02
		* ...
	* Season 6
		* Doctor Who (2005) - S06E01
		* Doctor Who (2005) - S06E02
		* ...

So within each TV series root folder you have a folder for each season labelled _'Season ...'_ and inside each season folder you have your episodes labelled _'TV Series name - S..E..'_. By using this convention you will ensure that XBMC is able to scrap you TV files without any problems. For files which span multiple episodes you can use _'TV Series name - S..E..-E..'_  e.g. Doctor Who (2005) - S05E01-E02.

Films are slightly easier and most of the time simply putting the full name of the film will provide results however I always place the year of release in brackets after the film name. e.g. 28 Days Later (2002). If you have a film that is spanned over a number of files you can make use of the following naming convention:

* Avatar (2009)
	* Avatar (2009) - Part 1
	* Avatar (2009) - Part 2  

This will allow XBMC to automatically switch to the necessary file during playback. 

This system has always worked extremely well for me and generally if I have problems its because I've made an error. However XBMC does support a number of different naming conventions and you can find out more by [clicking here][xbmcnaming].

*****

That is part 3 finished and for now a completion to this series of posts. I hope you have found it useful and at the very least a good starting point for building your own home theatre system. I'm sure that over time I will return and revise the information here as I continue to build and play around with what I have. If you like what I've written, please let me know via twitter or the comments below.



[dmmpart1]: http://dalemmanning.wordpress.com/2013/03/23/building-a-home-theatre-system-part-1/  
[dmmpart2]: http://dalemmanning.wordpress.com/2013/04/01/building-a-home-theatre-system-part-2/  
[ripitlink]: http://thelittleappfactory.com/ripit/  
[mdrplink]: http://www.macdvdripperpro.com  
[handbrakelink]: http://handbrake.fr
[wimowehlink]: http://www.serialangels.co.uk/wimoweh/wimoweh.html
[xbmcnaming]: http://wiki.xbmc.org/index.php?title=Video_library/Naming_files
[tvdblink]: http://thetvdb.com
[mvdblink]: http://www.themoviedb.org
