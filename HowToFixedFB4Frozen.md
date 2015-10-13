# Introduction #

since yesterday,my FB4Linux often be Frozen ,and eclipse to dead.
the eclipse log show this:

```
!ENTRY org.eclipse.ui 4 0 2009-11-26 16:28:13.702
!MESSAGE Unhandled event loop exception
!STACK 0
org.eclipse.swt.SWTException: Failed to execute runnable (org.eclipse.swt.SWTError: No more handles [MOZILLA_FIVE_HOME='/usr/lib32/xulrunner'] (java.lang.UnsatisfiedLinkError: no swt-mozilla-gtk-3550 or swt-mozilla-gtk in swt.library.path, java.library.path or the jar file))
        at org.eclipse.swt.SWT.error(SWT.java:3884)
        at org.eclipse.swt.SWT.error(SWT.java:3799)
        at org.eclipse.swt.widgets.Synchronizer.runAsyncMessages(Synchronizer.java:137)
        at org.eclipse.swt.widgets.Display.runAsyncMessages(Display.java:3468)
        at org.eclipse.swt.widgets.Display.readAndDispatch(Display.java:3115)
        at org.eclipse.ui.internal.Workbench.runEventLoop(Workbench.java:2405)
        at org.eclipse.ui.internal.Workbench.runUI(Workbench.java:2369)
        at org.eclipse.ui.internal.Workbench.access$4(Workbench.java:2221)
        at org.eclipse.ui.internal.Workbench$5.run(Workbench.java:500)
        at org.eclipse.core.databinding.observable.Realm.runWithDefault(Realm.java:332)
```


# Details #

this page has  deprecated,current FB4Linux have work in x64 without the ia32lib,it is Platform independent ,can work with x86 and x64.

~~this is not the FB4Linux bug,it's the bug of run win32 eclipse in x64 system,eclipse can't load xulrunner lib.~~

just install a i386 version xulrunner can fixed this:
  * sudo getlibs -p xulrunner-1.9.1 (ubuntu user:sudo apt-get install getlibs before.)
  * download libswt-mozilla-gtk-3555.so to /usr/lib32
  * cd /usr/lib/jvm/ia32-java-6-sun/jre/lib/i386 && sudo ln -s /usr/lib32/libswt-mozilla-gtk-3555.so
  * getlibs -l libxcb-atom.so.1
  * getlibs -l libxcb-event.so.1
  * getlibs -l libxcb-aux.so.0
  * getlibs -l libstartup-notification-1.so.0
  * getlibs -l libhunspell-1.2.so.0

  * add follow to eclipse run command:
```
export MOZILLA_FIVE_HOME=/usr/lib32/xulrunner-1.9.1.5
export LD_LIBRARY_PATH=/usr/lib32:/usr/lib32/xulrunner-1.9.1.5
```

by the way.if eclipse do not reply the mouse click,add follow to eclipse run eclipse:
```
export GDK_NATIVE_WINDOWS=1
```

more info:
http://blog.javaee.cz/2009/11/ubuntu-910-64bit-and-custom-32bit-jdk.html