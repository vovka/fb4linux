# Introduction #

this is a draft to make design work.


# Details #

Flash Builder's Desing view base the windows/mac's flash player,and depend on the FlashPlayer access dll.we can replace the dll with flash player linux,but we can't know the dll api.so  Not a Through Road.

so can we call the flash player dll by wine?this is the draft:

```
fb4linux<->socket<->fb4linux wine bridge<->flash player dll
```

or remote call by jini.

the way can make the profile work fine too!

i had do a Fb4linux Wine Bridge by java ,the source code to view the source

but i can't init the owl,it's got error 3

maybe,some adobe worker can help me?!
