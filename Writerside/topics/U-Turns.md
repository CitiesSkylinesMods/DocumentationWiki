# U-Turns

## Overview

Use these features to control where vehicles can make U-turns (180° turn, allowing them to travel back the way they
came).

Vehicles can do a U-turn at:

* The end of [dead ends / cul-de-sacs](https://en.wikipedia.org/wiki/Dead_end_(street))
    * This is vanilla game functionality, and is always enabled
* Junctions
    * This optional TM:PE functionality can be applied city-wide, and/or customized for each road at a junction

U-turns can help simplify and shorten vehicle routes, but at junctions they can disrupt oncoming traffic.

## Usage

There are two ways to enable U-turns at junctions:

* [](Junction-Restrictions.md), or
* [](Lane-Connectors.md) (create a link from an incoming lane to an outgoing lane on the same road)

> To use them, the features must be enabled in [](Maintenance.md) in [](Settings.md).

## Applicators

If you want to customize individual junctions, use either the [Junction Restrictions](Junction-Restrictions.md)
or [](Lane-Connectors.md) tool.

If you want to set the default for all junctions, use the **Vehicles may do U-turns at junctions** option
in [](Policies.md) in [](Settings.md).

Realistically, U-turns are impractical on smaller roads (which usually require
a [three point turn](https://en.wikipedia.org/wiki/Three-point_turn)). U-turns are best suited to medium/large roads,
particularly those with a central median.

## Technical

The vanilla game allows U-turns at **terminal nodes**. TM:PE allows you to extend that functionality to **transition
nodes** and **junction nodes**:

* U-turns can only happen if there is a left-pointing (RHD) / right-pointing (LHD) lane arrow
* Cars must be able to reach the turn lane.
* Check whether there are sufficient lane changing points in front of the turn lane.

If TM:PE is presented with multiple ways to turn a vehicle round — for example driving round the block vs. U-turn at a
terminal node vs. U-turn at a junction — it will favour the option with the fewest number of lane changes.

As a U-turn is technically always `1` lane change, vehicles would always U-turn at junctions and transitions. However,
this doesn't happen in real life; U-turns are cumbersome and sometimes dangerous, so drivers generally prefer a slightly
longer (easier and safer) route. To mimic this behaviour in game, TM:PE treats U-turns at transition and junction nodes
as `2` lane changes; drivers will look for a nearby alternative before doing a U-turn. This value is defined by
the `UTurnLaneDistance` setting in [Global Configuration](Global-Configuration.md). A lower value makes U-turns more
desirable, a higher value makes them less desirable.

## FAQ

**Does this affect frame rate or cause lag?**
> No. Although the pathfinder has to do a few additional checks (for U-turn settings) the increased availability of
> U-turn locations helps many vehicles find shorter paths to their destination.

**My city is a grid layout, should I use U-turns?**
> Grid layout provides lots of opportunities for vehicles to turn round, however U-turns might still be useful on some
> arterial routes — particularly in locations where there might be few alternate opportunities for vehicles to turn
> around.

## See also

* [](Lane-Changes.md)
* [](Nodes,-Segments,-Lanes.md)