# somfy-shades
SmartThings Somfy dth for zrtsI

There are two DTHs used to get zrtsI working

1) zwave wave controller for the somfy ZRTSI  (this is built into SmartThings)
2) This DTH, for the shades / blinds

This presumes shades/blinds are working with your Somfy TELIS remote control.  Ensure these are working before installing the zRTSII.  If there are issues, I suggest you contact Somfy support to ensure everything is working properly before setting up the zRTSII

Plug in the zWave RTSII Module into an outlet and follow the instructions to program your zWave Controller and blinds to your Smartthings controller (https://www.somfysystems.com/file.cfm/Zwave_to_RTS_instructions.pdf?contentID=284866). For the channels (Virtual Node), in the ST app, you do "Connect New Device", and then on the zWave RTS Controller, you add your virtual nodes. I had 5 virtual nodes, 4 blinds plus the "All Blinds: channel, They correspond to how my Telis remote is programmed. In my case, I now have 6 "things" show up (5 Blinds Channels and the controller).

The shades/blinds DTH supports both shades and blinds.  You need to go to settings in each devuce to set for shades or blinds.

The drawbacks of using SmartThings with Somfy are:

1) If you change the blinds with the physical Telis remote, ST will not know about the status. This is a limitation with how the zWave controller works and it doesn't report the status back to ST.

2) If you have an all channels device, the other devices don't sync when you use the 'all' device.  There is a SmartApp to address this:
https://community.smartthings.com/t/release-blinds-sync/46806

References:
https://community.smartthings.com/t/my-somfy-smartthings-integration/13492
