Introducing the ZWave Scene Controller plugin

This is an Indigo 7 plugin that I wrote early in the Indigo 7 beta process when developers had access to Zwave APIs but the UI hadn't been updated to support scene control. Since release, a number of users have made use of as new makes and models of scene controllers have come on the market that Indigo hasn't yet issued a device definition for.

For those wanting to jump straight in, the latest download link is always at the bottom of this post. 

Current Features
Provide triggers to act on button presses on scene controller devices
Log incoming scene commands (debug mode) to determine required values
Read-only support for Enerwave SCN7
Read-only support for Cooper RFWC5 - untested but should work!
Store the 'last pressed button' of a scene controller - and display in control pages

Coming soon
Interactive support for Enerwave and Cooper controllers - ie turn on the LED for a scene executed from Indigo
Store the 'last pressed button AND action' of a scene controller

Planned for later
-

Installation notes
This plugin creates a number of Trigger events under "Z-Wave Scene Controller events". You can combine these with indigo actions or action groups to perform device or scene activity upon press of a button. 

The new release (v1.0.19 and above) provides a new 'dummy' device type called Z-Wave Scene Controller > Scene Controller. Most users won't need to create a dummy device , but there's no harm in doing so. As well as providing support for the Enerwave and Cooper devices, these new dummy devices will store the last-called scene (button & action) from the device including ZRC-90's.

Enerwave and Cooper users MUST create a dummy device to represent their actual device. THEN, you need to go to Indigo > Plugins > Z-Wave Scene Controller > Setup Scene Controller. Pick your dummy device and the model and hit Execute. This links the device to Indigo. 

Known issues
Sometimes duplicate commands are received from Enerwave; I'm working on ignoring these but it's not straight forward. It's only a problem if you have triggers that toggle a device, as each duplicate will re-toggle the device back to its previous state,

Those who have seen me around the forums will know I usually participate in the forums at least daily if not several times; however please be aware this is usually from my iPhone when I'm away from my desk. I will endeavour to support this plugin as quickly as possible, but (as with everyone) I have busy periods of the year when I'm simply not at my desk long enough to do all I'd like to, including fixing or updating plugin code, even if you see me actively responding to other threads. 

Enjoy!

Peter