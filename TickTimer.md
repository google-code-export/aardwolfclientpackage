# Tick countdown timer (`Aardwolf_Tick_Timer.xml`) #

Estimates the time left until the next game tick in the MUSHclient status area. (see 'help tick')


## Where is it? ##

Down at the very bottom, underneath your input bar.
It says "Time to tick:" and then a number of seconds remaining.

![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/ticktimer.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/ticktimer.png)

## Why does it only update every 2 seconds? ##

Ticks aren't guaranteed to happen after exactly 30 seconds, and the timer isn't guaranteed to be ultra precise in all cases, so the countdown timer is set to a resolution of 2 seconds for psychological reasons. It is easier for the player to cope with ticks being off by a second or so if they expect the timer to only update coarsely.