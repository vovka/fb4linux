# Introduction #

The Flash Builder use the system language default.u can modify the eclipse.ini add -nl language code(english:en\_US  or chinese:zh\_CN) to modify the language.

for example,my eclipse.ini content:
```
-nl
en_US
-startup
plugins/org.eclipse.equinox.launcher_1.1.0.v20091023.jar
--launcher.library
plugins/org.eclipse.equinox.launcher.gtk.linux.x86_1.1.0.v20091012
--launcher.XXMaxPermSize
256m
-vmargs
-Xms512m
-Xmx1024m
-XX:MaxPermSize=256m
-XX:PermSize=64m
```