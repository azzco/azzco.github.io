---
title: Update to TTS Projector Mod 
category: TTS coding
---
Someone reported that my old workshop mod for Tabletop Simulator didn't work as expected. It's been about a year since I used it myself but I think I sorted it out.

# What is it?
The mod itself is quite simple. There's three components:
* Camera
* Modded tablet
* Projection plane

The camera is basically just a viewpoint directed at a in-game tablet. The tablet is modded to have a higher pixel density, higher resolution. The projection plane is basically a viewport, a 2d plane showing what the camera sees.

The idea is to have a smaller tablet showing a VTT map for TTRPG games, the map is then projected over the larger 2d plane that pretty much covers the game table.

# The problem
The higher resolution on the tablet is really needed, blowing up the image as large as the plane does provides a veeery blurry result with the default resolution.

When the tablet is loaded (onLoad) it sets the higher resolution. Now this isn't something I've tested but I suspect that if a player joins after that (pretty much expected to be the case really) they might have the default resolution since they missed the "update".

My workaround was to have this update baked into the show/hide buttons. A year after I used it last the buttons are not visible anymore. I don't know when but at some point it seems Tabletop Simulator dropped support for lua generated buttons. I couldn't see anything in the patch notes about that tough.

# The solution
XML buttons
This seems like a much better way to handle things, being able to rotate the ui elements in 3d could be really nice for a few cases. I would like to dig deeper into this at some point but this simple code seems to do the trick.

```xml
<Defaults>
  <text color="#FFFFFF"/>
</Defaults>
<button onClick="showBattleMap" position="-425,-615,-6.1" height="50" width="50" rotation="180 180 0">☐</button>
<button onClick="hideBattleMap" position="-375,-615,-6.1" height="50" width="50" rotation="180 180 0"></button>
```