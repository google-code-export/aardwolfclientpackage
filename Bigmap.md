# The bigmap window (`Aardwolf_Bigmap_Graphical.xml`) #

Display a graphical view of the continent bigmap. Optionally merge this display with the GMCP mapper window (this is the default behavior).


## What's a bigmap? ##
Back when the continents were created, Lasher decided that it would be nice to give people a way to visually appreciate them better. The 'bigmap' command lets you see the continent that you're currently on. See the in-game help file:
```
help bigmap
```

## What does this look like? ##
If you happen to be on Mesolar, it will probably look something like this

![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/bigmap.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/bigmap.png)

## Where am I on the bigmap? ##
You are here:

![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/bigmapme.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/bigmapme.png)

The inner box shows your current room. The outer border shows the range that you can see on the ASCII automap.

## Hey, my GMCP mapper got replaced by this bigmap picture when I walk onto the continents. What gives? ##
That is a major feature of this plugin. If you really don't like it, see below for options to change this behavior.

## Why did you do this? ##
Because before the GMCP mapper looked like this on the continents and had a less than stellar display. Here's just one example of why this addition makes sense.

![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/bigmapcompare.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/bigmapcompare.png)

I think the value of bigmap is obvious here.

## How do I change this plugin's behavior? / How do I get the standard GMCP mapper tile view back on continents? ##
You can control the bigmap either by commands listed in the help output or via a right-click menu.

To get a brief description of the available bigmap commands, type
```
bigmap help
```
![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/bigmaphelp.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/bigmaphelp.png)

### bigmap on/off ###

The off command makes the bigmap disappear. If you have the `bigmap merge` setting enabled (on by default) the gmcp mapper window goes back to the old display of showing individual room tiles that you can right-click on to change exits and add notes and stuff.

The on command makes the bigmap view come back, like for when you are done making manual changes.

### bigmap merge/unmerge ###

This controls whether the bigmap display will try to use the same miniwindow space as the gmcp mapper.

With the bigmap merged, you might see this:
![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/bigmapmerged.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/bigmapmerged.png)

With the bigmap unmerged, you might see this:
![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/bigmapunmerged.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/bigmapunmerged.png)

### right-click menu ###

The same options in the right-click menu look like this:

![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/bigmap_menu.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/bigmap_menu.png)

## I got a message saying "To activate this continent map, walk onto the continent and type: 'bigmap update'. What does that mean? ##
The message is only there as a precaution, since the plugin should take care of this for you automatically. But if the message persists, just do what it says.

Explanation: Before you can see the pretty continent picture like shown above, the plugin has to generate it based on the bigmap information from the game. This is how we do that.