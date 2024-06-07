> Article verified: August 2019

# Symptoms

These issues can affect trains, metros, monorails, trams, or any other tracked network (and sometimes bus routes too):

* Unable to create routes between stations ([example](https://steamcommunity.com/app/255710/discussions/0/1768134097428152371/))
* Vehicles not spawning on to routes

> If out-of-city cargo trains are spawning but passenger trains aren't, see: [Regional passenger trains not visiting city](Regional passenger trains not visiting city)

# Causes

> In the case of trains, please note that intercity trains (from out of town) can often still use broken tracks.

* Bend angles too sharp
* Wrong type of track for outside connections (breaks passenger trains)
* Gaps in tracks (often caused by mods that move or alter tracks or terrain)
* Track segments too short
* One-way tracks (select the track in the build menu and you'll see arrows on any existing one-way tracks)
* Missing depot connection (Trams, and also metros if using Metro Overhaul Mod)

# Solutions

### Sharp angles / gaps in tracks / tiny segments:

This issue mostly affects **train**, **metro** and **monorail**. Trams are much more forgiving, but can sometimes still be affected. On rare occasions, busses are also affected.

The easiest solution is to rebuild your tracks between the stations, using two-way tracks (not one-way), ensuring each segment correctly joins to the next (no gaps) and taking care to ensure bends are gradual and smooth (not sharp).

Gaps are sometimes, but not always, visible on the map:

![Gaps in tracks](https://i.imgur.com/yuqLHfi.jpg)

Note that if you use the 'straight track' tool when drawing tracks, it has a habit of creating sharp "angular" bends, which is bad for any kind of tracked vehicle. What you want is gradual, smooth curved bends. Either use the 'curved track' tool to draw your tracks, or use the [Move It!](https://steamcommunity.com/sharedfiles/filedetails/?id=1619685021) mod's curve snapping feature ([youtube tutorial](https://www.youtube.com/watch?v=pte_uz-3khg)) to smooth out your tracks.

Where possible, try and avoid tiny segments, particularly if using mods such as [Tiny Segments](https://steamcommunity.com/sharedfiles/filedetails/?id=1586027591), [Move It!](https://steamcommunity.com/sharedfiles/filedetails/?id=1619685021), or various anarchy mods.

### Trams

* Make sure all your tram routes have a connection to the Tram Depot (especially if you see a "not connected" notification over the tram depot).
* The depot will keep trying to reach the broken line, preventing it from delivering trams to the other lines.

### Trains (Passenger and Cargo):

* For **passenger trains**, only vanilla tracks can be used at the outside connections:
    * Tracks from the workshop do not generate the "fake station" that appears at edge of map
    * Solve this by using vanilla tracks for outside connection = you get the fake station
    * After the end of the fake station (you see an "X" crossing in the tracks) you can then start using workshop tracks again
* TM:PE users: Check your [](Vehicle-Restrictions.md) - if you ban certain trains from a section of track, is there an alternate route for them?
* Some station assets don't have spawn points, fix that with the [**Spawn Points Fix**](https://steamcommunity.com/sharedfiles/filedetails/?id=820157360) mod

### Metro with [Metro Overhaul Mod](https://steamcommunity.com/sharedfiles/filedetails/?id=816260433):

* Ensure you have a [Metropolitan Depot](https://steamcommunity.com/sharedfiles/filedetails/?id=816325876) building that's powered, watered and connected to both road and metro.
* Every metro station needs to be connected to the Depot so that trains from the Depot can reach the station.
* Metro station should be _smaller_ than 192 meters long (try 144m to see if that works).
* Ensure no sharp bends, they are particularly problematic with metro tracks!

### Broken and Ghost Nodes

There's a bug in vanilla game that can affect path finding, causing vehicles not to spawn or to despawn.

* Subscribe and enable [Broken Nodes Detector](https://steamcommunity.com/sharedfiles/filedetails/?id=1777173984)
* The workshop page describes how to use it
* Note that it now has extra features for finding and fixing ghost nodes, broken transport lines, etc - you'll see when you run it in-game.

# Fixed?

If not, try: [Vehicles not spawning](Vehicles not spawning)

Other issues? See: [Troubleshooting](Troubleshooting)