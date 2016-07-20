# VHS Public 3.0
This is the requirment for the System Varsio.

This is designed for Mac's Only

You can change this to fit your own program.  This is a third party framework to add external connection commands to your own terminal.  This is not to be used in any system default terminal.  In order to set change your permission to sudo at all times.

# Setup

In order to setup download the Rootfs.dmg.  You need to change this ot a read/write dmg by typing the following command,

cd (folder with rootfs.dmg)
hdiutil convert Rootfs.dmg -format UDRW -o RootfsRW.dmg

Once its a read and write then use the different contents for different parts of your terminal. Example,

Place this in your plugins folder if you are using Terminal Template 1.0 (Link Not Availble Build Your Self).  Then attach it to the main system file by adding this line of code,
```
import [VHS] from '../plugins/vhs';

..

command {[VHS], [other commands]} locate ({

  vhs-D=ALLOW
  [Other Commmands]
  
  )}
  
..
  
varsio.set = bundleVAR = VHS = FULLSUDO.ATrun
```
# Usage

The Usage is the following

./filesystem <Command> <Input> <Other>

For help on this project please input

./filesystem -help -all

For updating the filesystem please imput

./filesystem -update --check

Thank you for using VHS 3.0

The docs for creating your own project are at http://vhshacking.tk
