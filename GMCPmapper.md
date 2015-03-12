# GMCP mapper (`aard_GMCP_mapper.xml` and `aardmapper.lua`) #

A dynamically updated mapper that enables rapid navigation by storing room information in a SQLite database.




## What does it look like? ##
Probably something like this

![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/gmcpmapper.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/gmcpmapper.png)

## What do the different room colors mean? ##
Some special rooms have colors that tell whether they are a bank, shop, guild, questor, etc. You can see (and redefine) these color settings in the configuration options as explained below in "Are there any configuration options?"

The rest of the room colors are based on terrain. Right-clicking on a room gives you the option to change the color assigned to its terrain. Keep in mind that this will change the color of all rooms of that terrain type.

## Are there any configuration options? ##
Oh, yeah. Tons of them! See that little box in the top left corner of the mapper that looks like `[*]`? Click on that to bring up a display configuration menu. (Click on the `[x]` to close it again.)

In this menu, all of the items are clickable. If the item is a color, then a color picker dialog will come up. If the item is a number, then a number input dialog will come up. And so on.

![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/gmcpmapperconfig.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/gmcpmapperconfig.png)

## Are there any special commands for using the mapper? ##
Many! The mapper is one of the most complicated plugins you're ever likely to see written for Aardwolf and has a wide array of commands. Learning how to use every aspect of it may take some time, but you'll likely find it well worth your while. To see the entire command list, type
```
mapper help
```
and you'll see:
```
                              [GMCP Mapper Help]
+---------------------------------------------------------------------------+

AUTOMATIC MAPPER by Fiendish
** This is a very improved GMCP version of the original ATCP mapper by Nick Gammon.
** Some GMCP specific code added by Lasher.
** A few new features contributed by Spartacus.
** Many bugs squashed and major improvements made to the original design by Fiendish.

The window can be dragged to a new location by dragging the room name.
Your current room is always in the center with a bolder border.
LH-click on a room to speed-walk to it. RH-click on a room for options.

LH-click on the "*" button on the upper-left corner for configuration settings.
(click again on the [x] to close configuration)

                           Mapper Help Index
=============================================================================
 mapper help               --> Show this list
 mapper help all           --> Show the entire list of all mapper commands
-----------------------------------------------------------------------------
 mapper help config        --> Commands for configuring the mapper
 mapper help exits         --> Commands for managing exits
 mapper help portals       --> Commands for managing portals
 mapper help searching     --> Commands for finding rooms
 mapper help exploring     --> Commands to aid exploring
 mapper help moving        --> Commands for moving between rooms
 mapper help utils         --> Other utilitarian commands
=============================================================================


+---------------------------------------------------------------------------+
```

Typing any of the listed commands in the index above will bring up the specific commands for that topic. Explore the entire command set with.
```
mapper help all
```

## Where am I on the mapper? ##
Your current position is the room box in the middle with the bold outline in the color specified as "Our room" in the configuration menu.

## Can I right click anywhere? ##
You can right click on any of the rooms currently being displayed. This will bring up a small menu of room-related options.

![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/gmcpmapperright.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/gmcpmapperright.png)

## How do I get details about a room? ##
If you hover your mouse over any room, you will see a bubble pop up with information about that room.

![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/gmcpmapperbubble.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/gmcpmapperbubble.png)

Or if you're in the room you can use the command

```
mapper thisroom
```

and you'll see something like this

![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/thisroom.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/thisroom.png)

## When I go out on the continents the mapper looks different. What is this? ##

Are you confused about this?

![https://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/bigmapcompare.png](https://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/bigmapcompare.png)

Original versions of the package did not yet include the ability to show what is called the 'bigmap'. If you need access to the old gmcp map tiles on the continents (to add notes or change exits by mouse) you can toggle the bigmap view either by typing:
```
bigmap off
```
and
```
bigmap on
```
or through the right-click menu options

![https://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/hide_bigmap_menu.png](https://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/hide_bigmap_menu.png)

![https://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/show_bigmap_menu.png](https://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/show_bigmap_menu.png)

For more information on this see the page for [the merged Bigmap plugin](Bigmap.md).

## Can I block dangerous routes? ##

You can achieve this by assigning level locks to dangerous exits. To assign a level lock to an exit, right click on the "from" room (all exits are defined as being _from_ one room _to_ another) and choose **Change Exit Level Lock**.


![https://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/gmcpmapperexitlockmenu.png](https://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/gmcpmapperexitlockmenu.png)

Then select the exit from that room to which you want to add a level lock, and click OK.

![https://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/gmcpmapperexitlockdialog.png](https://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/gmcpmapperexitlockdialog.png)

Then choose your level to lock under. Keep in mind that these locks automatically take tiers into account. So a lock of level 50 will be open to a Tier 1 at level 40 and a Tier 5+ at level 1. The example below uses 300, which will always be locked for any level of any tier.

![https://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/gmcpmapperexitlocklevel.png](https://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/gmcpmapperexitlocklevel.png)

If you click OK, the chosen exit from the chosen room will be assigned the chosen lock level.

Locked exits display in the mapper in red instead of white.

![https://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/gmcpmapperexitlockmarking.png](https://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/gmcpmapperexitlockmarking.png)

## Configuring the norecall/noportal assistance ##

Understanding what this does:
Sometimes the shortest path from where you are to where you want to go starts with entering a portal, but you happen to be in a noportal room so that just won't work. Likewise, maybe the shortest path starts with a 'home' or 'recall' command, but you happen to be in a norecall room. When configured correctly the mapper can find the nearest walkable room that allows you to escape the prison and, if necessary, bounce through a portal to get to recall or bounce through recall to get to a portal destination.

  * **portalrecall** - Tells the mapper that a particular 'mapper portals' entry  won't work in a norecall room because it uses the home or recall commands.
  * **bouncerecall** - Bounce through this 'portalrecall' flagged mapper-portal in the scenario where the shortest path wants to enter a portal but you are in a noportal room.
  * **bounceportal** - Bounce through this non-recall mapper-portal in the scenario where the shortest path wants to recall or home but you are in a norecall room.

The steps for using the portalrecall, bouncerecall, and bounceportal commands may not be immediately obvious to everyone. Follow this example for configuring the mapper to robustly handle finding paths from noportal and norecall rooms.

  1. Type 'mapper portals' to show the list of your current portals and find index numbers

&lt;BR&gt;



&lt;BR&gt;

![https://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/mapperportalsexample.png](https://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/mapperportalsexample.png)
  1. Type something like 'mapper portalrecall 2' to mark a particular portal as using the home or recall game commands

&lt;BR&gt;



&lt;BR&gt;

![https://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/mapperportalrecallflag.png](https://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/mapperportalrecallflag.png)

&lt;BR&gt;



&lt;BR&gt;

recallportals will show up in red when viewing the 'mapper portals' list and the mapper will know not to use them from norecall rooms but that they are safe for noportal rooms

&lt;BR&gt;



&lt;BR&gt;

![https://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/mapperportalsrecallexample.png](https://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/mapperportalsrecallexample.png)
  1. Type something like 'mapper bounceportal 1' to mark a particular non-recall/home mapper-portal as being the command you always want to bounce through when the mapper wants to recall or home while you are in a norecall room. This interface may change in the future.

&lt;BR&gt;



&lt;BR&gt;

![https://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/mapperbounceportal.png](https://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/mapperbounceportal.png)

&lt;BR&gt;



&lt;BR&gt;


  1. Type something like 'mapper bouncerecall 2' to mark a particular recall-flagged mapper-portal as being the command you always want to bounce through when the mapper wants to use a handheld portal while you are in a noportal room.

&lt;BR&gt;



&lt;BR&gt;

![https://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/mapperbouncerecall.png](https://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/mapperbouncerecall.png)

&lt;BR&gt;



&lt;BR&gt;

Note: You will not be allowed to set an index as the bouncerecall command if it is not already flagged 'portalrecall' like above. This interface may change in the future.

## More Tips ##

User "Hosch" also has a nice little writeup about getting the most out of your mapper.

http://www.holgerschurig.de/games/aardmapper.html

# Database Corruption #

If either your computer or MUSHclient crashes, the database used for storing your mapper information may be left in an unusable and unrecoverable state. These situations are somewhat rare, but they can happen occasionally even on fairly stable computers. This is why the GMCP mapper plugin has a built-in facility for data integrity checks and daily rotating automatic backups as well as immediate manual backups.

Every 24 hours (or when you launch MUSHclient if more than 24 hours have elapsed) the mapper plugin will, by default, attempt to make a backup copy of the database file that stores your map and portal information in it. If you happen to be in combat when the backup wants to run, the mapper will notify you and then wait until combat has ended.

If the backup runs successfully you will see a message like:

![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/backupmsg.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/backupmsg.png)

If for some reason the backup or integrity check fails, you will see a message like one of the following:

&lt;BR&gt;


**FAILED INTEGRITY CHECK**

&lt;BR&gt;


**ERROR executing system command:**

&lt;BR&gt;


**ERROR (###) trying to copy database from `_____` to `_____`**

&lt;BR&gt;


or...well...pretty much anything else that looks bad and is obviously not a success message.

_If you ever see one of these error messages you may need to restore from a backup copy as described below._

If you see **ERROR (###) trying to `CreateDirectory`: `_____`** then the mapper tried and failed to make the db\_backups folder. You should fix the cause for this. It means you have MUSHclient in a place where, for some reason, it doesn't have access to make new folders.

If you like living life on the edge, you can disable automatic backups by using the command
```
mapper backups off
```

But this is a BAD idea. Please don't disable backups and then come crying to me that you lost all your data. "But I was saving space!" you will say. And I will say "You saved 100 megabytes. Congratulations. Now you have nothing." Seriously, this is like riding a bicycle without a helmet. You can point at all kinds of studies about risk-taking and injury rates for bicyclists with and without helmets, but one day you might hit your head. And if you ride without a helmet you will die. And it will be entirely your fault. Be safe. Backup.

If you need to save space and are willing to accept a slightly slower backup process, you can make it so that backups get .zip compressed with the command
```
mapper backups compressed
```

## Restoring From A Database Backup After Corruption ##

If you experienced a crash recently, you may find that your mapper database no longer works properly. That sucks but can be fixed as long as you have database backups.

First, quit MUSHclient. You should never rename or move around files while MUSHclient is running.

Then get rid of the damaged database files. These should be named Aardwolf.db (or something\_else.db if you've done something silly like making a new world file). The key to finding the right file is that the name of the database is the same as the world file that you use to connect to Aardwolf. The name of the default world file that everyone starts with in the Aardwolf MUSHclient Package is, conveniently, "Aardwolf". This makes the default mapper database file Aardwolf.db. So go find that file and delete it. You should also look for files named like Aardwolf.db-shm and Aardwolf.db-wal and delete those too if you find them.

Then look inside the **db\_backups** folder of your MUSHclient directory. You should find a collection of files with names that look like "blahblah\_Automatic" and "blahblah\_Automatic\_old" and "blahblah\_Automatic\_older", etc.

![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/backup_files.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/backup_files.png)

Make a copy of the most recent file (from BEFORE the crash) and put it in the same place where your old database file (the corrupt one you just deleted) was before in the MUSHclient directory. If you can't figure out when a backup file was made, you'll need to look at file modification dates. You can ask for help on the Tech channel in-game if you don't know how to do a google search.

You'll have to rename the backup file to match what your old database file was named before. So in the default case this means naming it "Aardwolf.db".

You may now restart MUSHclient.