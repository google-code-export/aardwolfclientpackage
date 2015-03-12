# Using MUSHclient on a Mac or Linux PC #



## It looks like MUSHclient is a Windows app. Is there a version for Mac or Linux? ##
The state of computers today is that Windows has had market dominance for so long that a lot of very smart people have spent a lot of time making it so that Windows apps can be run on Mac (though only on Intel CPU Macs) and Linux operating systems. Two primary methods are explained below -- running through [Wine](MacLinux#Running_MUSHclient_in_Wine.md) and running inside a [virtual machine](MacLinux#Running_MUSHclient_in_a_virtual_machine.md).

I (Fiendish) run the Aardwolf MUSHclient Package on both Linux and Mac OS (Intel). So yes, it is indeed possible to run this on all three major platforms. And it's pretty easy with a few small caveats that will be explained.

## Running MUSHclient in Wine ##
### What is Wine? ###
[WineHQ](http://www.winehq.org) describes it in the following basic way: "Wine lets you run Windows software on other operating systems. With Wine, you can install and run these applications just like you would in Windows."

You can also see the [Wikipedia entry for Wine\_(software)](https://secure.wikimedia.org/wikipedia/en/wiki/Wine_(software)) to learn more.

One of the major benefits of using Wine is that you do not need to install Windows.

### How do I install Wine in Linux? ###

Installing Wine in Linux is extremely straightforward with one minor caveat. If you are using an Intel graphics driver version between 2.12 and 2.15 (as of this writing) you'll probably need to use an old version of Wine (wine1.0 rather than wine), because of a bug in the Intel driver. It affects, for example, my Lenovo Thinkpad x201i running Ubuntu because it has an Intel graphics chip. If you have ATI or NVIDIA graphics, you should be fine with the latest version of Wine.


&lt;BR&gt;

See here: https://bugs.freedesktop.org/show_bug.cgi?id=28798


&lt;BR&gt;

**UPDATE**: Intel has fixed the driver bug, but it may take time to reach some distributions. There is a PPA that can be applied to fix Ubuntu 11 here https://launchpad.net/~smorar/+archive/bugfixes

Installing Wine in Linux is as simple and straightforward as installing anything else from the command line. Just open up a terminal and, for example...

In Ubuntu you could type:
> `sudo apt-get install wine`
In Fedora you could type:
> `sudo yum install wine`
In Gentoo you could type:
> `sudo emerge wine`
And so on...

### How do I install Wine on a Mac? ###
Requirements:
  * A Mac with an Intel CPU (All new Macs use Intel CPUs). Older PPC or 68k Macs cannot use Wine. Sorry.
  * (maybe) X11 (this is already installed by default on Snow Leopard and Leopard. If you are running Tiger, you can install X11 from your Tiger installation DVD using the "Optional Installs.mpkg" file. This may also be installed for you by other packages.)


Either http://www.playonmac.com/ or http://wineskin.urgesoftware.com/ are really good options for getting Wine running on your Mac.

If you're really adventurous, you can also try...

http://wiki.winehq.org/MacOSX/Installing

#### Last Resort Option for Macs (very simple to set up, but old and buggy) If You Can't Figure Out PlayOnMac/Wineskin ####

Probably the _simplest_ method to get Wine is as follows:
  1. Download a standalone Wine app from https://code.google.com/p/aardwolfclientpackage/downloads
  1. Find the file you just downloaded. It should look something like this: <img src='https://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/winedmg.png' align='center'>
<ol><li>Double click on the file and you should see a disk icon mounted on your desktop that looks like this: <img src='https://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/winemounted.png' align='center'>
</li><li>Double click on that icon and you should see a window that looks like this: <img src='https://aardwolfclientpackage.googlecode.com/svn/trunk/wiki_images/winewindow.png' align='center'>
</li><li>Drag the Wine icon onto the Applications folder as instructed by the arrow.</li></ol>

Once Wine is installed in this way, you can start MUSHclient by right-clicking on MUSHclient.exe and choosing Open With...->Wine.<br>
<br>
<h2>Running MUSHclient in a virtual machine</h2>

<h3>What is a virtual machine?</h3>
Unlike Wine, where you do not need to actually install Windows to use Windows software, setting up a virtual machine means essentially creating a whole virtual computer running a second operating system that runs inside of your main operating system. Popular virtual machine software for the Mac includes <a href='http://www.vmware.com/products/fusion/overview.html'>VMware Fusion</a>, <a href='http://www.parallels.com/products/desktop/'>Parallels Desktop</a>, and <a href='http://www.virtualbox.org/'>VirtualBox</a>. Of those three, <a href='http://www.virtualbox.org/'>VirtualBox</a> has the significant benefit that it doesn't cost anything because it is <a href='https://secure.wikimedia.org/wikipedia/en/wiki/Free_software'>free/open source software</a>.<br>
<br>
<h3>How do I install a virtual machine on a Mac?</h3>
Requirements:<br>
<ul><li>A Mac with an Intel CPU (All new Macs use Intel CPUs). Older PPC or 68k Macs cannot run modern virtual machine software. Sorry.</li></ul>

After installing your virtual machine host software, you will need to install Windows as a guest operating system. Whichever software you choose will walk you through this process. After installing Windows inside your virtual machine, you will have a fully functional secondary operating system inside of which you can then download and run the Aardwolf MUSHclient Package.