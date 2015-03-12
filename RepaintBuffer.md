# The repaint call buffer (`aard_repaint_buffer.xml`) #
https://github.com/fiendish/aardwolfclientpackage/blob/MUSHclient/MUSHclient/worlds/plugins/aard_repaint_buffer.xml

Executes a single Repaint call if multiple repaint requests are issued by various plugins in rapid succession. Required by included plugins for screen updates. Do not disable or remove this!



## Why does this exist? ##
Updating the screen in MUSHclient is a tricky art that involves juggling performance concerns with a desire for frequent immediate display refreshes. The problem I tried to address is as follows:

  * Calls to Redraw() may not get addressed soon enough due to heavy plugin processing.
  * Calls to Repaint() will always get addressed immediately, even if Repaint was already just called a single millisecond before.
  * Calls to Repaint() have performance consequences, slowing down the operation of MUSHclient if used too frequently.

This is explained in the documentation for [Redraw](http://mushclient.com/scripts/doc.php?function=Redraw) and [Repaint](http://mushclient.com/scripts/doc.php?function=Repaint)...

> "Unnecessary calls to Repaint will slow the program down."

&lt;BR&gt;


> "Redraw will cause the window to be redrawn at the next appropriate opportunity. Note that the main window is not actually redrawn at this point, however it is scheduled for redraw next time through the main event loop."

## So what does it do? ##
This plugin allows for deferred updates for better performance, like with Redraw, and also the higher priority of Repaint that causes it to happen at all instead of never when under heavy load.

## Does it work? ##
I think so. :)

## How do I use it in my plugins? ##
Most of the time you don't need to tell MUSHclient to refresh the screen. It will just happen on its own. So first consider carefully whether you need to worry about this at all.

If you're fine with using Redraw() given the described constraints, use that. If you're at all considering using Repaint(), though, do this instead:
```
BroadcastPlugin (999, "repaint")
```