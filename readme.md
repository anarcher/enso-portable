## Enso Portable

A portable distribution of the *community* version of Humanized Enso Launcher for Windows with some additional commands

(C) 2011-2012 g/christensen (gchristnsn@gmail.com)

v0.1.1

---

Description: the Enso Launcher application allows to launch programs found in the Windows Start menu (or picked manually using the `learn as open' command) and perform many other operations with text command line, 
triggered by pressing the CAPSLOCK key. It's possible to create your own commands using the Python programming language.

[Download](https://github.com/downloads/GChristensen/enso-portable/enso-portable.7z.sfx.exe) the portable binary distribution (no installation is required).

Background: I haven't found any Enso command package suitable for my needs, so I decided to make my own one. If you like Enso, you can use the source code freely as you wish, see more at the [Enso Launcher page](http://humanized.com/enso/launcher).
The source code of the original community Enso application could be found here:
[https://launchpad.net/enso/community-enso](https://launchpad.net/enso/community-enso) 

The GIT repository contains only the Enso source code without a Python interpreter, it's more convenient to use the binary package above (which includes a trimmed down Python interpreter) to develop your own commands, so you need only the Notepad to do this.

To add a new command you need to put a Python file with its source code into the `commands' folder under the Enso root directory (see the [docs](https://github.com/GChristensen/enso-portable/blob/master/enso/docs/enso-docs.txt) on command authoring).

####Dependencies

* Abbyy Lingvo dictionary software (optional)


####Additional functionality not found in the original Enso

* Ability to restart using a tray menu item or the `enso restart' command


####Additional Commands 

>>**session.py**

>>>Session/Power management commands (self explanatory):
      
>>>* log off
* shut down
* reboot
* suspend
* hibernate

>>**system.py**

>>>System commands:

>>>* kill [process name or id] - kill a process using its executable name
                                   (without extension) or id

>>**dial.py**

>>>Dial-up network related commands:
  
>>>* dial [connection name] - connect to the Internet using a dialup connection
* hangup [connection name] - close an Internet connection

>>**idgen.py**

>>>Generate a UUID in several formats (upper/lower case, numeric):

>>>* guid [format]

>>>Generate a random number in the Int32 positive range [0, 2147483646].
    It's possible to narrow the range using command arguments:

>>>* random [from num to num]

>>**lingvo.py**

>>>Control Abbyy Lingvo dictionary software with Enso Launcher. It's possible to specify translation direction attributes, see command help for the details.
     
>>>* lingvo [word from lang to lang] - translate a word
>>>* quit lingvo - close Lingvo

>>**mount.py** <font color="red">warning: does not work out of the box, hacking required</font>

>>>A set of shortcuts to [un]mount TrueCrypt volumes:

>>>* truecrypt mount [letter] - mount a truecrypt volume assigned to the specified letter 
* truecrypt umount - unmount all mounted volumes

>>**wake.py** <font color="red">warning: does not work out of the box, hacking required</font>

>>>Wake on LAN related commands (requires terminal access to a [dd-wrt](http://www.dd-wrt.com) router):

>>>* wake slave - send a magic packet to a workstation with MAC address hardcoded in the command file

>>**wireless.py** <font color="red">warning: does not work out of the box, hacking required</font>

>>>[dd-wrt](http://www.dd-wrt.com) router wireless management commands:

>>>* switch wireless - turn wireless radio on/off
