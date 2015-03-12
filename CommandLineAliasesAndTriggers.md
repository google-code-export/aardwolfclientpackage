

# How do I add aliases and triggers from the command line like I can in `<other_client>`? #

MUSHclient does not by default have a mechanism for creating aliases and triggers from the command line. This is likely because of a combination of the possible complexity of setting up any given alias or trigger and the fact that more and more people are moving towards using plugins for everything.

But the fact remains that sometimes a player wants to be able to set up simple aliases and triggers quickly and easily without dealing with the rather complicated interface and without having to write a full plugin.

It is possible to add this functionality to MUSHclient by adding two aliases (described down below):
```
#alias {*} {*}
```
for adding new simple aliases, and
```
#trigger {*} {*}
```
for adding new simple triggers.

If you are using the world file included in recent versions of the Aardwolf MUSHclient Package, then you may already have these aliases.

## How do I check to see if I have these aliases already? ##

You can check by going to the Aliases configuration screen by pressing Shift+Ctrl+9 or by going to Game->Configure->Aliases... as shown here:

![https://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/gamemenu.png](https://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/gamemenu.png)

## I don't have these aliases yet. How do I make them? ##

The process for adding these is as follows:

1. Select all of the text in the box below and copy it. Typically this is done either with Ctrl+C or by right-clicking on the selected text and choosing "Copy".
```
<aliases>
  <alias
   match="#alias {*} {*}"
   enabled="y"
   group="special_convenience_aliases"
   send_to="12"
   sequence="100"
  >
  <send>require "addxml"  -- addxml extension

-- add the alias

addxml.alias {  
  match = "%1", 
  send = "%2",
  sequence = 100,
  enabled = true,
  send_to = 10,
  group = "command_line_aliases"
             }

ColourNote ("white", "green", "Added alias to match on '%1', sending '%2'")
  </send>
  </alias>

  <alias
   match="#trigger {*} {*}"
   enabled="y"
   group="special_convenience_aliases"
   send_to="12"
   sequence="100"
  >
  <send>require "addxml"  -- addxml extension

-- add the trigger 

addxml.trigger {
  match = "%1", 
  send = "%2",
  sequence = 100,
  enabled = true,
  send_to = 10,
  group = "command_line_triggers"
               }

ColourNote ("white", "green", "Added trigger to match on '%1', sending '%2'")
  </send>
  </alias>
</aliases>
```

2. Go back to MUSHclient and bring up the Aliases configuration screen by pressing Shift+Ctrl+9 or by going to Game->Configure->Aliases... as shown above.

3. On the Aliases configuration screen, find the Paste button and click it:

![https://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/aliasesconfig.png](https://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/aliasesconfig.png)

![https://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/aliasesconfig2.png](https://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/aliasesconfig2.png)

You should now have both aliases in place. Click OK to go back to the game.

## Now how do I use these aliases? ##

Say you want to make an alias where the pattern is:
```
h *
```
and you want the result to be (where %1 is the target you want to heal):
```
cast 'heal' %1
```

You would now be able to type:
```
#alias {h *} {cast 'heal' %1}
```

And then you could, for example, do:
```
h self
```

which would result in sending:
```
cast 'heal' self
```

### Multiple commands in one alias ###

If you want to perform multiple commands with a single alias, you need to use  two semicolons (;;) to separate the commands as in:
```
#alias {h *} {cast 'heal' %1;;say I just healed %1!}
```

For the reason why, [read about semicolons in MUSHclient here](FAQ#How_do_I_send_a_literal_semicolon?.md).