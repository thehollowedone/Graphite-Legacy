
[![forthebadge](https://forthebadge.com/images/badges/fuck-it-ship-it.svg)](https://forthebadge.com) [![forthebadge](https://forthebadge.com/images/badges/you-didnt-ask-for-this.svg)](https://forthebadge.com) [![forthebadge](https://forthebadge.com/images/badges/built-with-resentment.svg)](https://forthebadge.com)

 ***Graphite*** was created as a way to prevent malicious Lua payloads from running funky code on your client.
 This was to be a 'legacy' version before I was to re-code an official version using API commands from a software provider who was interested.

Most 'game-fuckery' in Garry's Mod is achieved with [RunConsoleCommand](https://wiki.facepunch.com/gmod/Global.RunConsoleCommand)/[ConCommand](https://wiki.facepunch.com/gmod/concommand.Add), which allows Lua to run commands in your Developer console to primarily change settings and attempt to save them. 

Garry (*I hopefully assume)* knew this was abusable as fuck but still opted to allow a pretty open ended access to the console **besides these commands listed**  [here](https://wiki.facepunch.com/gmod/Blocked_ConCommands). 

Graphite was created as a secondary-layer of protection and logging of what servers *really* are running on your client. This also does work as a secondary form of protection against any 'bypass' that might make it's way past `FCVAR_SERVER_CAN_EXECUTE`

I originally posted this in Pastebin in March 2019, but I figured I could make it more 'accessible' via GitHub and add more comments to what I'm actually doing in my code. I warn you however as this is technically possible to detect if an anti-cheat developer knows how to properly check for Detours.

*SHOUTOUTS:*

**Anubis**

Gave the initial inspiration for this project after I saw his projects, [Aegis & Iron Curtain, (broken link)](https://github.com/ProjectOdium/OdiumLua)

**c0deine** 

Created the [base code for the Detour system](https://pastebin.com/zXAUKBg2) that Graphite uses, even though I've 'modified' how the protection functions. 

**AVexxed**

 Alerting me to a detour detection method (Which isn't fully patchable in pure Lua as far as I know, this will just stop brainlet anti-cheat developers but won't stop meep <3)

**triggered**

Initial help with un-fucking the script after I had coded myself into a hole with no way out.



*FUCKS TO:*

**garry newman**

Why do you make people pass booleans as a string and then convert them on the client automatically?

**roberto ierusalimschy** 

If the fact that concatenating a variable argument looks like `..(...)` doesn't bother you, I don't know what kind of psychopath you are.

