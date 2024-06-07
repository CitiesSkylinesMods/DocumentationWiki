> Verified: March 2022 - TM:PE 11.6.5.1

# Symptoms

> Note: These issues can also occur on pedestrian paths

One or both of the following occurs:

* When I rotate the map, the road texture flickers (usually at junctions)
* Grass or other terrain artefacts are showing through roads (usually at junctions or connections between different kinds of road)

# Causes

This issue is _not_ caused by TM:PE.

Both symptoms are caused when the ground terrain isn't fully underneath the road. This is most common at junctions, road transitions (eg. between elevated and ground, or different types of road), and level crossings.

# Solutions

The most common solution is to use the [Move It!](https://steamcommunity.com/sharedfiles/filedetails/?id=1619685021) mod to move nodes to more level terrain or raise/lower nodes so they cause the terrain to conform in a more uniform manner. Moving nodes further apart often helps too.

An alternative is to use terrain-clipping [surfaces](https://steamcommunity.com/sharedfiles/filedetails/?id=1762784478) or [networks](https://steamcommunity.com/sharedfiles/filedetails/?id=1516956630) ([different widths version](https://steamcommunity.com/sharedfiles/filedetails/?id=1875956729)), as illustrated below:

![Terrain clipping surface](https://i.imgur.com/YUM7kIv.gif)

Those networks or surfaces just remove the terrain completely, which can solve the flickering problem and also remove any grass or other stuff showing through the road. You'll need to use Move It mod to precisely align and position them under your road.

For junctions on roads and tracks, particularly if the terrain is sloped, try and ensure that nearby nodes are exactly the same height (you can do that using Move It mod to align heights). Alternatively, you can use [Node Controller](https://steamcommunity.com/sharedfiles/filedetails/?id=2085403475) or [Node Controller Renewal](https://steamcommunity.com/sharedfiles/filedetails/?id=2472062376) (only subscribe one, not both!) to fine-tune the nodes, for example to make them sloped, tilted, etc.

# Fixed?

If not, see if any of these guides help:

* [Section of road becomes blue void](Section of road becomes blue void) - when using "Adjust Roads" info view
* [Blue void roads or tracks](Blue void roads or tracks) - when placing buildings that contain road/track
* [Blue void showing near roads](Blue void showing near roads) - also applies to paths, tracks, etc.

Other issues? See: [Troubleshooting](Troubleshooting)