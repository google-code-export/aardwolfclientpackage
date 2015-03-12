

# How do I write triggers in MUSHclient? #

Scripting is a complicated subject that has been addressed by documentation for MUSHclient itself. See the following pages for some help on writing triggers:

  * [MUSHclient documentation: triggers](http://www.mushclient.com/scripts/doc.php?general=triggers)
  * [Introduction to scripting](http://www.mushclient.com/forum/?id=6030)
  * [Making a simple trigger](http://www.mushclient.com/forum/?id=8086)
  * [Making a script to count mobs killed](http://www.mushclient.com/forum/?id=8411)
  * [Video showing how to make a trigger](http://www.mushclient.com/forum/?id=9626)
  * [Scripting function list](http://www.mushclient.com/scripts/doc.php?general=function_list)
  * [Complete online documentation for MUSHclient](http://www.mushclient.com/scripts/doc.php)

# I tried making a trigger but it isn't firing. What did I do wrong? #

In zMUD, if you make a pattern that looks like

```
This is a pattern
```

It will match on

```
HELLO This is a pattern FROM THE FUTURE!!!
```

Because zMUD's standard pattern format is sloppy and begins and ends with implicit `"*"`.

MUSHclient works differently. MUSHclient's standard pattern format treats your pattern as if it begins with `"^"` and ends with `"$"`. There is no implicit allowance for extra garbage outside of the pattern. In MUSHclient if you want to catch

```
HELLO This is a pattern FROM THE FUTURE
```
and also just
```
This is a pattern
```
Then you would need to make your pattern something like
```
*This is a pattern*
```

Or switch to using [regular expressions](http://mushclient.com/scripts/doc.php?general=regexp), which are much more expressive (but are similarly trickier to get right).

# How do I make multi-state triggers? #

See this forum post explaining how to translate the zMUD/CMUD multi-state trigger concept into MUSHclient triggers:

http://www.mushclient.com/forum/bbshowpost.php?bbsubject_id=10338

# zMUD lets me add triggers from the input bar. How do I do that in MUSHclient? #

See the guide page on that subject here:

https://code.google.com/p/aardwolfclientpackage/wiki/CommandLineAliasesAndTriggers