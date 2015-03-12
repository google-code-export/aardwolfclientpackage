# Teach me about miniwindows! #

Ok. Let's cover this in two sections...
  1. The practical interaction with miniwindow plugins in the Aardwolf MUSHclient Package.
  1. A brief technical overview of what it means to call something a miniwindow.



## Miniwindows in the Aardwolf MUSHclient Package ##

Miniwindows in the package all share certain characteristics with each other that are introduced in tips #2 and #3 of the center of the [welcome message box](NewConnection.md) that pops up the first time you run the package.

![https://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/newconnectioncircled.png](https://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/newconnectioncircled.png)

### Dragging/Moving ###

All of the miniwindows in this package can be moved around the screen, so that you can organize your layout any way you want.

http://www.aardwolf.com/play/screenshots.htm has many screenshots with examples of this.

In order to move the miniwindows around, find the part of the miniwindow where the mouse cursor changes to a hand and then click and drag. This part is either the entire miniwindow or a bar across the top if the rest of the area is used for other click actions. The hand looks like this: <img src='https://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/handcursor.png' align='top'>

<h3>Resizing</h3>

Nearly every miniwindow in this package is in some way resizable to your own preference by dragging the resize widget in the lower-right corner of the miniwindow. The resize widget looks like this: <img src='https://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/resizer.png' align='top'>

When you move the mouse over the resize widget, the cursor will change to a pair of opposing diagonal arrows to indicate that the miniwindow can be resized by dragging there, like this: <img src='https://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/resizecursor.png' align='top'>

<h3>Right click Pop-up Menus</h3>

All of the miniwindows in this package have special menus that pop up when you right-click on them. These windows can contain configuration options and other commands that let you interact with the plugin in useful ways.<br>
<br>
Here's just one example:<br>
<br>
<img src='https://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/comlogright.png' />

<h3>Controllable Z-order</h3>

Z-order is the order in which miniwindows are drawn on top of each other. In traditional coordinates, X is left/right, Y is up/down, and Z is in/out of the screen. A new feature in the plugins included in this package is the ability to make any of them jump in front of or behind all the others. In the example below, the player has the channel capture window hiding behind the ASCII map.<br>
<br>
<img src='https://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/zorderexample1.png' />

Selecting "Bring To Front" from the right-click menu on the channel capture window allows the player to switch the display order so that it gets shown on top. "Send To Back" (not shown) will do the reverse.<br>
<br>
<img src='https://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/zorderexample2.png' />

<img src='https://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/zorderexample3.png' />

<h3>Lockable Layout</h3>

You can lock and unlock your miniwindow layout at any time. See here for more information:<br>
<br>
<a href='http://code.google.com/p/aardwolfclientpackage/wiki/Layout#How_do_I_lock_my_layout?'>http://code.google.com/p/aardwolfclientpackage/wiki/Layout#How_do_I_lock_my_layout?</a>

<h2>Miniwindows: A Technical Overview</h2>

A "miniwindow" is the MUSHclient term for using a region of the screen for graphics, text, and mouse-event handlers that are technically part of but visually distinct from the main text output from the game.<br>
<br>
<a href='http://mushclient.com/mushclient/mw_intro.htm'>Click here for an introduction to using miniwindows in your own scripts.</a>

Miniwindows are not actually windows, though they can be made to behave like windows. They are in fact technically just elaborate blocks of pixels drawn on top of the main output area. The very first miniwindows were all stuck in place, fixed size, and nearly monochromatic. As time went on and developers got more used to the idea, we started inventing cool new features until eventually they started being less like fixed rectangular blocks and more like actual windows with intricate graphics and mouse event handlers. Advanced miniwindows today can simulate resizing and dragging and highlighting text, even though technically they are still just blocks of pixels pretending to be windows.