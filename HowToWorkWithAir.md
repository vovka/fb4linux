# Introduction #

the flex sdk 's air is mac version default,so if u run the air app in fb4linux or run the flex sdk adl command,u'll got the can't run a binary file.

to fiexed it,u must got the air sdk for linux from http://airdownload.adobe.com/air/lin/download/latest/air_1.5_sdk.tbz2 ,and extract to the flex sdk dir:

```
wget http://airdownload.adobe.com/air/lin/download/latest/air_1.5_sdk.tbz2
tar xjf air_1.5_sdk.tbz2 -C $FLEX_SDK_ROOT
```