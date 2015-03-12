# Main output windower and layout control (`aard_layout.xml`) #

Sets up the main output as a movable, resizable region instead of filling the whole client. It creates a desktop-like space that automatically adjusts the line wrap column when the main output area is resized. It also allows you to lock down the position and size of cooperative miniwindows.



## What's this about? ##

Well, you see, normally MUSHclient looks like this...

![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/mushclientnowindow.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/mushclientnowindow.png)

The text is always attached to the far left and goes all the way up to the top, and control of where the lines wrap is hidden behind a configuration screen that isn't very intuitive.

With this plugin, however, the main output area can be moved away from the top left if desired (this is especially useful if you want to put other miniwindows across the top of the screen without losing text behind them that will mess with scrolling up), and the line wrap column automatically adjusts to fit the width of the area chosen by the user.

![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/mushclientyeswindow.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/mushclientyeswindow.png)

## How do I lock my layout? ##

To lock the current miniwindow layout, type
```
aard layout lock
```

To unlock the current miniwindow layout, type
```
aard layout unlock
```

To check the current layout lock status, type
```
aard layout
```

## Where is the scroll bar? ##

It's not attached to the text area anymore. Sorry. Look over at the very far right side of your MUSHclient window. Actually, that's exactly the same place it was before. This is just how MUSHclient's TextRectangle feature works. `*shrug*`

![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/mushclientyeswindowscroll.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/mushclientyeswindowscroll.png)

## So how do I move this output area around and resize it? ##

Even though this is not actually a miniwindow ([click here for boring technical details](http://mushclient.com/scripts/doc.php?function=TextRectangle)), resizing and moving are done basically in the same way as with all of the miniwindow plugins. The bottom right corner has a widget for resizing, and there's a draggable part across the top of the box for moving it around. Just look for where the mouse cursor changes to a hand.

## I can't see the resize widget! It went off the screen and now I can't see incoming text! Help! ##
Try typing:
```
resetaard
```