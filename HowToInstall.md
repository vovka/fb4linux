# Introduction #

how to install the Adobe Flash Builder™ 4.5 For Linux.

# System Requirements #

  * eclipse 3.6+
  * java 1.6+

# Details #


  * Download the two FB45ForLinux install file from downloads page((u can use the md5sum to check the download file)
  * if u download before 2011-10-14,please download the file again!the last version is support i386&amd64!
  * use cat command the merge the two file to one install file:
```
cat FB45ForLinux* >FB45ForLinux.tar.bz2
```
  * extract it.for example,extract to:/home/feiy/FlexBuilder45Linux
  * in eclipse,select Help->Software Updates->Manage Configuration(if u no this menu,todo:select Window->Preferences->General->Capabilities-> checked Classis Update) ->right click->add->extension location->select the path :/home/feiy/FlexBuilder45Linux
  * submit,reboot eclipse.

## other ##

if can't run/debug app,do:

install the debug version flashplayer plugin .the fb45linux don't check the debug plugin.

if u want run/debug air app,do:

download the air sdk for linux,and extract the the flex sdk dir.