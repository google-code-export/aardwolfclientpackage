# Communication Log window (`aard_channels_fiendish.xml`) #

This plugin captures channels and other bits of information to a floating miniwindow so that you can follow conversations more easily.



## What does the communication log window look like? ##

It should look something like this:

![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/comlog.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/comlog.png)

## What options are available if I right-click? ##

There are many different right-click options.

![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/comlogright.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/comlogright.png)

### Copy Selected / Copy Selected Without Colors ###

If any text inside the log window is selected, this text will be copied to the clipboard either with or without Aardwolf color codes inserted. More on selecting later.

### Copy All ###

Copies the entire capture buffer to the clipboard. This is like Copy Selected but grabs everything instead of just the selected text.

### Change Font ###

Changes the display font.

### Timestamp > ###

You'll notice in the above example image that captured messages are marked with the date and time. You can change the format of this timestamp, or disable it, by choosing one of the options in this sub-menu.

![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/comlogtimestamp.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/comlogtimestamp.png)

### Customize Channels ###

By default all channels are captured to the communication log window. You can use this option to change which channels get captured and which ones don't. In the following example, all channels except for auction and debate are being captured:
![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/choose_captured_channels.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/choose_captured_channels.png)

### Capture Other Info > ###

Some informational messages on Aardwolf do not present themselves in the form of channels with GMCP data. Other things may be annoying under certain circumstances. Control of those bits go here.

![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/comlogother.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/comlogother.png)

INFO:, Global Quest:, and Remort Auction: can be optionally captured by enabling or disabling the right options. If you are in a clan with members who all have gold donation triggers, you might also desire to specifically disable the capturing of clan donation messages.

### Echo Channels In Main Window > ###

By default, all lines that get captured to the communication log window also get shown in the main output. Use this submenu if you want to change that.

![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/echo_channels_menu.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/echo_channels_menu.png)

### Logging to File > ###

The channel capture plugin has the ability to record a log of all captured messages to a text file in the MUSHclient\logs folder.

If the Remove Timestamps option is not enabled, your chosen timestamp will be included in the log.

If the Remove Color Codes option is not enabled, the log will include Aardwolf color codes in colored text.

![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/comloglogging.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/comloglogging.png)

## How else can I interact with the channel capture window? ##

Aside from the standard resizing (drag the bottom-right corner) and moving (drag the title bar), there are a few other things you can do.

### Open URLs in your web browser ###

Right-clicking on a captured URL presents two new menu options, "Go to URL" (which will launch your default web browser) and "Copy URL to Clipboard".

![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/chat_url_menu.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/chat_url_menu.png)

### Scroll up and down ###

You can scroll up and down inside the channel capture window by any of the following methods:

  * mouse-wheel scrolling with the cursor placed inside the miniwindow
  * clicking on the up/down arrows at the top-right and bottom-right of the miniwindow
  * dragging the miniwindow's scrollbar shuttle

### Select captured text ###

The channel capture miniwindow, through the magic of awesomeness, supports selecting arbitrary bits of text with the mouse. Just select it as you would select text anywhere else. After you have text selected, you can copy the selection to the clipboard with or without Aardwolf color codes via the right-click menu.

![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/comlogselect.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/comlogselect.png)

### Send your own custom lines to the log window ###

There is a function in the plugin, called `storeFromOutside` that makes it easy to log arbitrary lines of colored text in the communication log window. You use it via the `CallPlugin()` access function, with input of a string with embedded Aardwolf color codes (example below).

For documentation on `CallPlugin()`, see http://mushclient.com/scripts/doc.php?function=CallPlugin

Example:
```
CallPlugin("b555825a4a5700c35fa80780","storeFromOutside","HELLO@RHello@Mhello@x215hello@x66HELLO")
```

![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/store_from_outside.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/store_from_outside.png)

To get Aardwolf color codes from a table of MUSHclient styles, see the function [StylesToColoursOneLine(styles\_table) in aardwolf\_colors.lua](http://code.google.com/p/aardwolfclientpackage/wiki/AardwolfColors#StylesToColoursOneLine_(styles,_start_column,_end_column)).

## Creating multiple log windows ##

If you want to have multiple log windows, each capturing different channels, you should take the following steps:

  1. Go into your plugins folder and find `aard_channels_fiendish.xml`
  1. Make a duplicate of that file (copy/paste) in the same folder. Give the duplicate any name you want, as long as the new file keeps the same .xml file type.

&lt;BR&gt;



&lt;BR&gt;

![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/duplicate_comm_log_plugin.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/duplicate_comm_log_plugin.png)
  1. In MUSHclient, go to the `Edit` menu and select `"Generate Unique ID..."`

&lt;BR&gt;



&lt;BR&gt;

![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/unique_id_menu.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/unique_id_menu.png)
  1. Copy the number in the small window that pops up and then click `Close`.

&lt;BR&gt;



&lt;BR&gt;

![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/unique_id.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/unique_id.png)
  1. Open the duplicate file you just made in a text editor like Notepad and find the bit near the top of the file that says `id="b555825a4a5700c35fa80780"`

&lt;BR&gt;



&lt;BR&gt;

![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/comm_log_id.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/comm_log_id.png)
  1. Replace the id string with the new one generated above.

&lt;BR&gt;



&lt;BR&gt;

![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/comm_log_change_id.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/comm_log_change_id.png)
  1. Save and close the file.
  1. Load your newly modified plugin into MUSHclient. If you don't know how, see [How do I load new plugins?](http://code.google.com/p/aardwolfclientpackage/wiki/FAQ#How_do_I_load_new_plugins?).
  1. You should now have another Communication Log window. Make sure to customize them (see the [Customize Channels](ChannelCapture#Customize_Channels.md) and [Capture Other Info](ChannelCapture#Capture_Other_Info_>.md) sections above) so that they don't capture the same channels.

&lt;BR&gt;



&lt;BR&gt;

![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/two_comm_logs.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/two_comm_logs.png)