# The group monitor window (`aard_group_monitor_gmcp.xml`) #

Displays the status of all of your current group members.


## What does it look like? ##

There are a number of different similar forms the group monitor window can take. The long answer is that it depends on how you've sized the window, because the plugin attempts to automatically arrange group members to fit logically into the available space. The organization algorithm it follows is that it starts with a single column, and then if there is enough room for additional columns it will create new columns if the creation of those columns would also reduce the number of rows.

#### My head exploded. Can you show examples? ####

Let's say you have 4 people including yourself in a group. It might look something like this:

![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/group1.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/group1.png)

But you could also resize the window so that it is shorter and wider. Then the group members could display like this instead:

![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/group2.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/group2.png)

Or you could go even wider and shorter. Then you could end up with this:

![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/group3.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/group3.png)

## My group is really big and I don't have a ton of space on my screen. Is there anything I can do? ##

There are a few things you can do, and they all involve using the right-click menu, so let's investigate those options.

## What are the right-click options? ##

![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/groupright.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/groupright.png)

### Change Font ###
Changes the display font.

### Show Players > ###
This submenu will show a list of all players currently in your group and offer the ability to selectively to show or hide any of them from the group monitor window.

#### Show Players > Include Self ####
You may choose to not show yourself in the group monitor window, since you already get personal status bars as a separate floating window. This will let you save some space.

![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/groupincludeself.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/groupincludeself.png)

### Configure Colors > ###
This lets you customize what border and fill colors are used for the various status bars. The "align" colors do not affect any bars. They are used to color the player names depending on whether the player is neutral, evil, or good alignment.

### Show Info > ###
Maybe you don't care about tracking group members' mana or moves, and you only want to know about Health. You can use these options to disable/enable some or all of the group member status bars. This will let you save some space.

If you disable mana and moves, for example, then the group would show like this:

![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/grouphp.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/grouphp.png)

### Use Flat Gauges ###
This option changes the display style for the gauges from the gradient shaded bars to flat ones.

![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/groupflatgauges.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/groupflatgauges.png)

### Overlay Numbers ###
This option makes it so that the HP, MN, and MV numbers show on top of their respective bars instead of along side them. This takes up less horizontal space.

![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/groupoverlaynumbers.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/groupoverlaynumbers.png)

### HP Thresholds > ###
You may want player hp gauges to change colors when they drop below certain thresholds. Here you can specify up to two different health percentages after which the hp bars will change to a different color.

![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/grouphpthresholds.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/grouphpthresholds.png)

![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/groupthresholdwindow.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/groupthresholdwindow.png)