# Nodes, Segments, Lanes

> Verified: December 2021 - TM:PE 11.5.2

## Overview

In Cities: Skylines, vehicles and cims travel along routes (roads, tracks, etc.) which have been placed on the map:

* Routes consist of one or more **Segments**
* Segments contain one or more **Lanes**
* Segments are joined togehter by **Nodes**

This article explains some of the nuances and terminology relating to them.

## Segments

Each route consists of one or more segments, joined by nodes. Each segment has a node at both ends, even if not joined
to other segments, and may curve and/or elevate between those two nodes.

> Mods such as [Node Controller](https://steamcommunity.com/sharedfiles/filedetails/?id=2085403475)
> and [Node Controller Renewal](https://steamcommunity.com/sharedfiles/filedetails/?id=2472062376) also allow the ends
> of segments to be _twisted_ and _stretched_.

![Segment with node either end](picNodesSegmentsLanes_segment.png)

Depending on the asset, there will be several segment styles ("elevations" / "prefabs") available:

* **Ground** (G) - segment follows or flattens the terrain
* **Elevated** (E) - small raised section or short bridge
* **Bridge** (B) - robust bridge, can span long distances
* **Slope** (S) - transition between tunnel and other elevations (i.e. it's the tunnel entrance)
* **Tunnel** (T) - fully underground

> Tip: For great looking bridges, try this sequence of segments: G→E→B→E→G (depends on the particular road as to how
> well it works)

## Lanes

**Segments** contain one or more **Lanes**, on which vehicles can travel.

![Lanes](picNodesSegmentsLanes_lanes.png)

> Technically, there can also be non-vehicle lanes, upon which nothing can travel, for example road-side prop lanes,
> tree lanes, medians, etc.

[](Lane-Changes.md) cannot occur in the middle of a segment; they can only occur at nodes. While _road
vehicles_ can change lanes at each node along a route, _tracked vehicles_ can only change lanes at junctions and
stations.

There are three common lane configurations within segments:

* **One-way** - all lanes travel in one direction
* **Two-way** - equal number of lanes in each direction
* **Asymmetric** - different number of lanes in each direction

## Nodes

A node is a point on a route between one or more segments.

### Ghost nodes

Nodes should always be connected to at least one segment. However, due to issues with some mods (like old anarchy mods),
it's possible to get nodes that aren't connected to anything. These are known as **Ghost nodes** (sometimes also
referred to as **Orphan nodes**).

![Ghost node](picNodesSegmentsLanes_ghost.png)

Ghost nodes are problematic because mods assume there will always be a segment attached; this can cause crashes or
annoying `Array index` errors.
Use [Broken Nodes Detector](https://steamcommunity.com/sharedfiles/filedetails/?id=1777173984) mod to remove ghost
nodes.

### Terminal nodes

**Terminal nodes** occur at the unconnected end(s) of a segment:

![Terminal node](picNodesSegmentsLanes_terminal.png)

Routes which end in a terminal node are called '[dead-ends](https://en.wikipedia.org/wiki/Dead_end_(street))' or '
cul-de-sacs'.

#### Roads (Terminal)

* [](U-Turns.md) can always be performed on terminal nodes
* [](Pedestrian-Crossings.md) (no road markings) are always enabled

#### Tracks (Terminal)

* Trains can't use dead-end tracks
* Any train on a dead-end track will ultimately despawn
* This also applies to monorail, tram, trolleybus, and metro

> You could use "empty" or "blank" station assets, which contain a station but no building, to give appearance of
> tracked vehicles using dead-end tracks.

### Middle / Segment nodes

**Middle nodes** (sometimes called **Segment nodes**) seamlessly connect two segments together:

![Seamless node](picNodesSegmentsLanes_seamless.png)

#### Roads (Middle)

* [](Lane-Changes.md) can occur
* Pedestrians can join nearby pedestrian paths from these nodes

#### Tracks (Middle)

* Trains must go straight-ahead at these nodes
* This also applies to monorail, tram, trolleybus, and metro

### Bend nodes

When two segments join at sharp angles, they sometimes create a **Bend Node** (depends on settings of the road asset):

![Bend node](picNodesSegmentsLanes_bend.png)

At first glance, a **bend node** looks like a **middle node**. However, on closer inspection that's not the case:

* The node acts like a virtual segment:
    * It copies the style of one of the adjacent segments
    * It's still a node, even though it looks like a segment
* The two segments either side are shortened slightly to accommodate the virtual segment

#### Roads (Bend)

* [](Lane-Changes.md) can occur
* [](Pedestrian-Crossings.md) (no road makrings) are enabled by default

#### Tracks (Bend)

* AVOID!!
* Bend nodes are likely to break the vehicle AIs

### Junctions with two segments

they occur between segments of different kinds of road. Generally, if there are different number of lanes, or the other
road is different size or elevation, you'll get a junction instead of a bend/middle node:

> todo: image

#### Roads (Two-Segment Junctions)

* [](Lane-Changes.md) can occur
* [](Pedestrian-Crossings.md) (with road markings) are enabled by default
* [](U-Turns.md) are disabled by default
    * Unless one of the segments is one-way; otherwise there is no way to reach the other side of the two-way road

#### Tracks (Two-Segment Junctions)

* Every incoming lane will be connected to every outgoing lane of the other segment

### Asymmetric nodes

Asymmetric nodes occur where asymmetric roads change direction (basically a stylised middle node):

> todo: image

#### Roads (Asymmetric)

* [](Lane-Changes.md) can occur
    * Vehicles in the terminated lane _must_ merge in to one of the remaining lanes
* [](Pedestrian-Crossings.md) are disabled by default
* [](U-Turns.md) are disabled by default

#### Tracks (Asymmetric)

* Currently, there are no asymmetric tracks available
* They would likely behave the same as tracked transition nodes

### Junction nodes

Junction nodes occur at the confluence of three or more segments of road or track (not both):

> todo: image

#### Roads (Junction)

* [](Lane-Changes.md) can occur
    * Vehicles can change to any outgoing lane
* [](U-Turns.md) can optionally be allowed
* [](Pedestrian-Crossings.md) (with road markings) are enabled by default
* Vanilla: Traffic Lights and Stop Signs can be used for additional control

#### Tracks (Junction)

* [](Lane-Changes.md) can occur
* Vanilla: Stop signs can control right-of-way

### Level crossing nodes

**Level Crossings** are **Junction Nodes** with both _road_ and _tracked_ segments; they can only occur at ground level:

> todo: image

Only one type of traffic can use the junction at a time; either road vehicles or trains. To enfore that, level crossings
have barriers that block road traffic from entering the junction while a train is approaching or crossing the junction.
The barrier will only lift once the train has fully cleared the junction (it's no longer on a tracked segment either
side of the junction).

#### Roads (Level Crossing)

* [](Lane-Changes.md) can occur
    * Vehicles can change to any outgoing _road_ lane
    * Vehicles cannot cross the tracks while barrier is down
* [](U-Turns.md) are disabled
* [](Pedestrian-Crossings.md) (no road markings) are enabled by default
    * Pedestrians cannot cross the tracks while barrier is down

#### Tracks (Level Crossing)

* Trains must go straight ahead at the junction
    * _I have no idea what happens if someone tries adding 3+ tracks to the junction_

## Nodeless networks

As mentioned at the start of this guide, segments always have a node at each end. Well, _that's not entirely true_.

Some workshop road and track assets provide **Nodeless networks** which allow segments to connect to junctions without
the side effects of having a node:

* The benefit is that the end of the segment won't be distored by the junction node; this facilitates some innovative
  design opportunities for asset creators and detailers
* The downside is that some traffic management features, such as stop signs and traffic lights, aren't available on the
  nodeless networks.

### Nodeless Examples

The [RWY](https://steamcommunity.com/sharedfiles/filedetails/?id=1569088356) project uses nodeless tracks to achieve
much nicer-looking junctions (top is normal junction, bottom is nodeless):

![Nodeless train tracks](picNodesSegmentsLanes_nodelessTrain.png)

The [LRT](https://steamcommunity.com/workshop/filedetails/?id=1560202570) project includes a sinking tram track,
achieved by having two roads (an avenue road and a tram road) on top of each other:

![Nodeless tram tracks](picNodesSegmentsLanes_nodelessTram.jpeg)

The [CSUR](https://steamcommunity.com/workshop/filedetails/?id=1959216109) project offers pick-and-mix nodeless networks
to achieve extremely flexible urban roads:

[![Nodeless CSUR roads](http://img.youtube.com/vi/C_QHwUnh430/0.jpg)](http://www.youtube.com/watch?v=C_QHwUnh430 "Watch on Youtube")

## See also

* [](Enter-Blocked-Junctions.md)
* [](Lane-Changes.md)
* [](Pedestrian-Crossings.md)
* [](U-Turns.md)