

# How do I make macros in MUSHclient? #
There are two ways of creating macros in MUSHclient, one of them is much more flexible but the other is a bit easier to use if its limitations don't impact your needs.

## Macro: The easy but limited way ##
The simplest way of creating macros is through the Macros and Keypad configuration dialogs. You can find them by pressing
```
Shift+Ctrl+2
```
and
```
Shift+Ctrl+1
```
or by using the menu options
```
Game->Configure->Macros...
```
and
```
Game->Configure->Keypad...
```

There you will find a set of predefined key combinations that you can use for sending various commands to the MUD. The limitations are that you cannot create new key combinations in these dialogs other than the ones that are already there, and you cannot process any kind of script functions.

## Accelerator: The more complex and more powerful way ##
The more flexible way to create macros is through a scripting feature called Accelerators. Accelerators can be made for any key combination and are overall more flexible in what they can do, though in order for them to persist you have to stick them inside a plugin because otherwise they go away when you quit.

The MUSHclient FAQ has an entry on creating accelerators that you should read here:

http://www.mushclient.com/forum/?id=7794#39

You may also want to read the relevant documentation:

http://mushclient.com/scripts/doc.php?function=Accelerator


&lt;BR&gt;


http://mushclient.com/scripts/doc.php?function=AcceleratorTo

# I tried assigning a macro to F1, but that just brings up the Windows Help App #
See this FAQ entry about how to fix that:

https://code.google.com/p/aardwolfclientpackage/wiki/FAQ#How_do_I_disable_F1_as_being_the_help_macro?