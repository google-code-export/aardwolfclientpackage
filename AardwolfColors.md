# Aardwolf color functions (`aardwolf_colors.lua`) #

A lua snippet file that provides functions for handling Aardwolf color codes to any plugin that wants to use them.



## How do I use this in a plugin? ##
If your plugin lives in the plugins folder, put this line somewhere in the main script body of your plugin:
```
dofile (GetPluginInfo (GetPluginID(), 20) .. "aardwolf_colors.lua")
```
Then use the provided functions as if they were part of your plugin.

## What functions does it provide? ##

### `StylesToColoursOneLine (styles, start_column, end_column)` ###
Converts all or part of a single line of MUSHclient style runs into a string containing Aardwolf color codes, starting at column start\_column and ending at column end\_column. To convert the entire line use 1 for start\_column and some sufficiently high number for end\_column like 99999. You may also leave start\_column and end\_column nil which will default to this behavior. Negative column indices will count back from the end of the line with -1 being the last character, but add a bit of performance overhead. Very large positive numbers are therefore going to be slightly more efficient than -1 for going all the way to the end, hence the default 99999 behavior.

### `ColoursToStyles (text)` ###
The reverse of StylesToColoursOneLine. This takes a string containing Aardwolf color codes and generates a sequence of MUSHclient style runs.

### `strip_colours (text)` ###
Takes a string containing Aardwolf color codes and removes all of the color codes from it.

### `stylesToANSI (styles)` ###
Converts a series of style runs to a string with embedded ansi codes.

## Will this handle xterm 256 colors? ##
Yes it will in all versions after [r397](Versions.md).

## Why do you use both the American and British spellings of "color"? ##
Because screw you, that's why!

## Why dofile instead of the cleaner require? ##

Purely [hysterical raisins](http://www.catb.org/jargon/html/H/hysterical-reasons.html).

## Why don't the function names follow a consistent pattern? ##

See the above two answers.