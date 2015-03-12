# Copy with color codes (`aard_Copy_Colour_codes.xml`) #

Allows you to copy text from the main output with Aardwolf color codes inserted in the right places.



## How do I use it? ##

When you select text from the main output, use Ctrl+D instead of Ctrl+C to capture color codes while copying.

If, for example, you selected the following output:

![http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/colorcopysource.png](http://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/colorcopysource.png)

Ctrl+C would result in

<pre>
Zcrim stops holding Aylorian Academy portal.<br>
Zcrim holds The Head of Medusa in his hand.</pre>

And Ctrl+D would result in

<pre>
@wZcrim stops holding @YAylorian @CAcademy @Wportal@w.<br>
@wZcrim holds The @RH@read @wof @GM@gedusa@w in his hand.@w</pre>

## Will it also copy xterm 256 colors? ##

Yes. xterm color support is provided for this plugin automatically by the special [color code handler](https://code.google.com/p/aardwolfclientpackage/wiki/AardwolfColors) included in the package.