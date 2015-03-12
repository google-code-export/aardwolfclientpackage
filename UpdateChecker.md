# Automatic Update Checker (aard\_package\_update\_checker.xml) #

This plugin enables the Aardwolf MUSHclient Package, if you choose, to automatically check for new beta versions from this google code repository every time you launch MUSHclient.



## Enabling update checks ##

The very first time you launch a new copy of the Aardwolf MUSHclient Package you should see this message:

![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/update_check_first_run.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/update_check_first_run.png)

Choosing `[`Yes`]` will enable update checks. Choosing `[`No`]` will not.

At any time during play you can change your mind as indicated in the message by simple installing or removing the Aardwolf\_Package\_Update\_Checker plugin (aard\_package\_update\_checker.xml).

## Can I make the update check run more often than once per startup? ##

The plugin has the following built-in command for that:
```
package update check
```

## How do I know when there is a new version available? ##

If the update checker plugin finds a new update, you will see a message pop up like this one:

![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/update_check_updates.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/update_check_updates.png)

### What happens if I choose `[`Ok, Show Me`]`? ###

Choosing `[`Ok, Show Me`]` will launch your default web browser to this URL which will always allow you to download the newest beta release:

https://code.google.com/p/aardwolfclientpackage/downloads/detail?name=MUSHclient.zip

### What happens if I choose `[`Ignore`]` or press Esc or just close the message dialog? ###

If you choose to ignore the update message, you will not be informed about updates again until another beta version is released. As a reminder of this policy, you will be shown a message similar to this one:

![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/update_check_ignore.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/update_check_ignore.png)

## How does it check what version I have? ##

It uses the `AardwolfPackageChanges.txt` file in your MUSHclient directory. Please never modify this file.