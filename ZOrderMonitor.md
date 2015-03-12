# Miniwindow Z-order Monitor (`aard_miniwindow_z_order_monitor.xml`) #

This plugin handles keeping track of the Z ordering of the miniwindow plugins included in the package and any other plugins that choose to use this ordering system.



## What is Z-order? ##
See the Wikipedia entry on Z-order here: https://en.wikipedia.org/wiki/Z-order

## How do I make the included miniwindows change ordering? ##

All of the included miniwindow plugins have right-click menu options 'Bring To Front' and 'Send To Back'.

![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/zordermenu.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/zordermenu.png)

## How do I make my own miniwindow plugins make use of your Z-ordering system? ##
If you want another miniwindow to fit into the Z-order system, there are only a few steps (the following assumes that the name of your miniwindow is stored in a variable called win)...

  * The name of your miniwindow must only contain numbers, letters, and the underscore character. Using the plugin UID as your miniwindow name is fine, for example.
  * After any call to `WindowCreate` and BEFORE you subsequently call `WindowShow`, you need to do
```
  CallPlugin("462b665ecb569efbf261422f", "registerMiniwindow", win)
```
  * You need to have an `OnPluginBroadcast(msg, id, name, text)` function that includes the following in case the z order monitor plugin gets reloaded
```
  if (id == "462b665ecb569efbf261422f" and msg==996 and text == "re-register z") then
     CallPlugin("462b665ecb569efbf261422f", "registerMiniwindow", win)
  end
```
  * You need to add this section of code (or if you already have an `OnPluginListChanged` function, you need to work this code in) to make sure that the z order monitor plugin is up and running when your plugin goes through `OnPluginInstall` at startup.
```
  require "checkplugin"
  function OnPluginListChanged()
     do_plugin_check_now("462b665ecb569efbf261422f", "aard_miniwindow_z_order_monitor")
  end
```

  * Once all of that is done, you can bring your miniwindow to the front of the stack by calling:
```
  CallPlugin("462b665ecb569efbf261422f","boostMe", win)
```
> and send it to the back by calling:
```
  CallPlugin("462b665ecb569efbf261422f","dropMe", win)
```
> How you choose to do that is up to you, but I recommend adding a right-click `WindowMenu` with 'Bring To Front' and 'Send To Back' options.