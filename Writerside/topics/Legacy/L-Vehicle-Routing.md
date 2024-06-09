# 👴 Vehicle Routing

> 👴 This article's content is old, copied from the original Wiki at https://tmpe.viathinksoft.com/wiki/

## Introduction

Traffic Manager: President Edition implements a custom lane routing algorithm in order to provide

1. more realistic lane changing patterns at road junctions and transitions ([junctionTransitionRouting](#)),
2. finer-grained control over permitted lane changes at junctions and on regular road segments
   (see [](Lane-Arrows.md) and [](Lane-Connectors.md)),
3. a stricter set of lane merging and splitting rules targeting highway interchanges
   (see [](Highway-Junction-Rules.md)),
4. improvements regarding overall road utilization and congestion avoidance
   (see [](Advanced-Vehicle-AI.md)), and
5. a feature that enables vehicles to adapt their behavior in accordance to the current traffic situation
   in realtime (see [](L-Dynamic-Lane-Selection.md)).

While modified junction routing rules (currently) take effect as soon as TM:PE is being activated
all latter features can selectively be enabled or disabled by the player at any time.

## Associated Features

* [](L-Junction-and-Transition-Routing.md)
* [](Highway-Junction-Rules.md)
* [](Lane-Arrows.md)
* [](Lane-Connectors.md)
* [](Junction-Restrictions.md)
* [](L-Modified-Path-Finding.md)
* [](Advanced-Vehicle-AI.md)
* [](L-Dynamic-Lane-Selection.md)

## Feature Timeline

As you may see in the image, the different lane selection features operate at different instants of time.

> _image is lost_
>
> The feature timeline of TM:PE. Though all features affect the overall game experience they perform their work at
> different instants of time.

### One-time calculations

The functions

* [](L-Junction-and-Transition-Routing.md),
* [](Lane-Arrows.md),
* [](Lane-Connectors.md), and
* [](Highway-Junction-Rules.md)

modify vehicle routing decisions as soon as the structure of the road network changes
(e.g. when the player builds or upgrades roads) or when the player interacts with TM:PE's tools
(e.g. by setting up lane arrows). As long as the network structure does not change and the player
does not interact with TM:PE, previous routing decisions made by these features are persisted
for later reuse.

### During path-finding

Since the [](L-Modified-Path-Finding.md) algorithm (and thus also the [](L-Advanced-AI.md))
is incorporated into the base path-finding algorithm it affects vehicle behavior at the time
when a route to a destination is being queried by any agent (e.g. citizen, vehicle) in the
game. Depending on the number of active agents requiring a new path, up to several hundred
path-finding requests are being dispatched within each second.

### During main simulation

The [](L-Dynamic-Lane-Selection.md) (DLS) feature enables real-time routing adaptions, that
means it operates alongside with the agent simulation. Every moving vehicle that uses DLS
to optimize its route performs one DLS execution per traversed road segment.

### Cross-cutting features

Three of the four available [](Junction-Restrictions.md) affect vehicle routing at different moments:

* The Vehicles going straight on may change lanes at junctions policy modifies routing
  information as soon as the player (de)selects the feature in the [](Settings.md) dialog or sets
  it for individual junctions.
* Both the Enable/Disable crosswalks feature and the Vehicles may do U-turns at junctions
  setting affect routing decisions at path-finding time.
* The Vehicles may enter blocked junctions restriction does not have any impact on lane selection.

> ☝️ `Traffic (Cities: Skylines Wiki) <https://skylines.paradoxwikis.com/Traffic>`_
