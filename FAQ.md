# MUSHclient Configuration / Frequently Asked Questions #

For the most part, as configured by default, you should be able to just run the program and start playing without any changes. But maybe you want to customize things a little bit to match your taste, and you don't know quite where to look.



## Where do I look for configuration and triggers and stuff? ##

The main configuration area of MUSHclient is accessible through the Game menu. Go to Game->Configure

![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/gamemenu.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/gamemenu.png)

All of the options under this menu will just bring up different sections of the same world configuration screen.

![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/configscreen.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/configscreen.png)

## How do I write Triggers, Aliases, or Macros? ##

[Click here to visit the page on writing triggers.](Triggers.md)

[Click here to visit the page on writing aliases.](Aliases.md)

[Click here to visit the page on writing macros.](Macros.md)

## How do I save a plugin from the MUSHclient forums? ##

First recognize that a plugin is a specially formatted ".xml" (as opposed to .txt or .doc) text file. You can frequently get these files by either downloading them or by copy/pasting them from forum posts on the [MUSHclient forums](http://www.mushclient.com/forum).

To save a plugin from a thread in the forums, do the following:
Copy all of the quoted lines of code from the forum entry. It probably begins with
```
<?xml version="1.0" encoding="iso-8859-1"?>
```
and ends with
```
</muclient>
```
Open a text editor (such as Notepad) and paste the plugin into it.

Save to disk on your PC, preferably in your plugins directory, as "your\_desired\_plugin\_name.xml" (ending in .xml is important!)

## How do I load new plugins? ##

Press `Shift+Ctrl+P` or go to `File->Plugins...` to bring up the `Plugins` dialog box.

Then click the `Add...` button and go find the plugin file you want to load.

![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/add_new_plugin.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/add_new_plugin.png)

## How do I make commands stay on the input line after I hit enter? ##

Go to Game->Configure->Commands... as shown above.
Then check the box for "Auto-repeat Commands".

## How do I make my number pad send numbers instead of north/south/east/west/etc? ##

Go to Game->Configure->Keypad... as shown above.
Then uncheck the box for "Enable Keypad Keys".

## How do I change the main output font? ##

Go to Game->Configure->Output... as shown above.
Click on the "Font..." button and choose a new font.

## How do I get rid of the bubble that shows line numbers and dates? ##

Go to Game->Configure->Output... as shown above.
Uncheck "Show Line Information".

## Can I make it so that text automatically gets copied to the clipboard when I select it, without having to do Ctrl+C? ##

Yep. Go to Game->Configure->Output... as shown above.
Check "Copy selection to Clipboard".

#### Can I get Aardwolf color codes with that? ####

Nope. Sorry. But see the page on [the included plugin for copying with color codes](ColorCopy.md).

## How do I disable F1 as being the help macro? ##

That's stored in a different place than most configuration settings.
Go to File->Global Preferences... and click on the General tab. Then check the box for "F1, F6 are macros". This will also let you use F1 as your own custom macro if you want.

![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/filemenu.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/filemenu.png)

![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/preferencesgeneral.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/preferencesgeneral.png)

## Where is the main output scroll bar? I can't find it! ##

[See the answer to this question here.](https://code.google.com/p/aardwolfclientpackage/wiki/Layout#Where_is_the_scroll_bar?)

## I don't like that the input bar automatically resizes. How do I change that? ##

Honestly, I think you're wrong to want to change this, and I too thought it looked a bit funny when I first started using it. There are absolutely no down sides to the auto-resizing input bar, only benefits. Please try it for a few days, let yourself get used to it, then come back and thank me. If you still don't like it after a few days of use, try the next section.

### Ok, I tried it out for a while and I still hate that the input bar automatically resizes. Yes, I know I'm wrong. ###

As long as you gave it an honest chance, here are all of the things you can do to modify the way the input bar works...

Press Ctrl+I or go to Game->Immediate... and in the window that pops up you can use one or more of the following script commands

Deactivate resizing (1 re-activates it)
```
SetOption ("auto_resize_command_window", 0)
```
Set the minimum height to, for example, 2 lines (default 1)
```
SetOption ("auto_resize_minimum_lines", 2)
```
Set the maximum height to, for example, 30 lines (default 20)
```
SetOption ("auto_resize_maximum_lines", 30)
```

For more details on these and other secret configuration options, see this page:

http://www.mushclient.com/forum/bbshowpost.php?bbsubject_id=10430

## How do I lock my layout so that I don't accidentally drag my miniwindows out of place? ##
See here for details on that feature of the layout plugin:

http://code.google.com/p/aardwolfclientpackage/wiki/Layout#How_do_I_lock_my_layout?

## How do I remove or change the Aardwolf logo background image in the main output? ##
The image file being used is `MUSHclient/worlds/plugins/images/aardbg13.png`

To have the image not show, either rename or remove that file. To change the image, just replace it with a new one.

## How do I send a literal semicolon? ##
Semicolon is the default line-break character for MUSHclient. In order to send a literal ; without having it eaten, you need to type two of them.

`;;` becomes `;`

`;;;;` becomes `;;`

And so on.