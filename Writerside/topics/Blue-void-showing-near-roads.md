# Blue Void Showing Near Roads

> Verified: March 2022 - TM:PE 11.6.5.1

## Symptom

* "Blue void" gaps are appearing on or near roads, paths or tracks

## Cause

This is _not_ caused by TM:PE.

To reduce graphic rendering load, the game removes terrain under roads and buildings. Normally you don't notice this
because those terrain gaps are covered by the road or building. However, in some cases, they become exposed, and you get
a "blue void" hole in the map due to terrain tearing.

The most common causes are:

* Zooming out causes road LODs to be displayed, which don't completely cover the clipped terrain
    * This is particularly common on roads that cut through mountains or other sloped terrain
* Networks (roads, paths, tracks) of differing height are placed too close to each other
* Very sharp junctions where there isn't enough room to 'fill the gaps' with terrain
* Networks crossing over each other or in very proximity
* Buildings or other features locking terrain height near a road

Sometimes the network (road, path, tracks...) are the problem, causing part of the network to turn in to a "terrain
hole". Common causes are placing a bus stop, or zooming out (junctions sometimes turn blue). Here's an example of a road
that doesn't properly handle bus stops:

![Road tearing due to broken bus stop mesh](https://i.imgur.com/qCFuPJh.png)

## Solutions

If the road asset is the problem, as described above, you'll just have to use a different road. Also, please let the
author of the road know about the problem - hopefully they can fix it.

For all the other causes...

The most common solution is to use the [Move It!](https://steamcommunity.com/sharedfiles/filedetails/?id=1619685021) mod
to move nodes to more level terrain or raise/lower nodes, so they cause the terrain to conform in a more uniform manner.
Essentially, you adjust the network to the terrain to avoid causing terrain tearing.

Alternatively, you can take the approach of adjusting the terrain to the network:

* [Extra Landscaping Tools](https://steamcommunity.com/sharedfiles/filedetails/?id=502750307) - flatten or smooth the
  terrain around networks; for best results smooth about 1-2 zoning tiles of terrain either side of the network
    * This is the best way to deal with those long terrain tears you see on distant roads when zoomed out
* [Terrain Flattener](https://steamcommunity.com/sharedfiles/filedetails/?id=1468227932) - these invisible parks just
  create completely flat terrain where they are placed
* [Terrain conforming network](https://steamcommunity.com/sharedfiles/filedetails/?id=1480409620) - it's a bit like an
  invisible road that causes terrain to conform to its height; vehicles won't use it and, importantly, it doesn't clip
  the terrain underneath it and like roads it can be used on slopes

If none of those things work, manually create your own terrain. This is most commonly achieved with the following mods
or assets from the workshop (you'll need
the [Find It!](https://steamcommunity.com/sharedfiles/filedetails/?id=837734529) mod to access them, and Move It! mod to
put them in the right place):

* [Ploppable Asphalt+](https://steamcommunity.com/workshop/filedetails/?id=1258162457) - provides dozens of flat surface
  shapes and sizes in different textures
* [Surface Networks](https://steamcommunity.com/sharedfiles/filedetails/?id=1875956729) - the network equivalent of
  Ploppable Asphalt
* [Slope Profiles](https://steamcommunity.com/sharedfiles/filedetails/?id=1674146668)
  and/or [Natural Slope Profiles](https://steamcommunity.com/sharedfiles/filedetails/?id=1708707788) - similar to
  Surface Networks, but they slope down at the edges

Another alternative is to place rocks, trees/bushes, props or some other asset over the terrain tears to hide them.

## Was it Fixed?

If not, see if any of these guides help:

* [](Section-of-road-becomes-blue-void.md) - when using "Adjust Roads" info view
* [](Blue-void-roads-or-tracks.md) - when placing buildings that contain road/track
* [](Road-texture-flickers,-or-terrain-showing-through-roads.md)

Other issues? See: [](Troubleshooting.md)