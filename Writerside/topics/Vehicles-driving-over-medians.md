> Article verified: June 2019

> Want to stop vehicles doing u-turns at junctions? See: [Junction Restrictions](Junction Restrictions)

# Symptom

* Vehicles are driving over medians or central barriers
* This can also apply to bus routes

# Cause

This issue is not caused by TM:PE.

The vanilla game has no concept of medians at junctions, which is why highways were implemented two separate one-way roads.

TM:PE provides features that allow you to gain more control over where vehicles can go, so you can work around this issue of the base game.

> **Asset authors:** The [**```NetInfo.m_CanCrossLane```**](https://cslmodding.info/asset/network/) does not prevent vehicles crossing medians; it's primarily designed for small roads (with no medians) and determines whether vehicles can cross lanes of oncoming traffic to reach a destination:
> * ```true```: Allowed
> * ```false```: Disallowed  

# Solution

* First, unsubscribe any [Broken Road Assets](Broken Road Assets) - these will cause issues no matter what you do
* Use [Lane Connectors](Lane Connectors) or [Lane Arrows](Lane Arrows) to precisely control where vehicles can go
    * The **Straight Ahead** feature  of the lane connector is often useful for this

# Fixed?

If not, please let us know: [Report a Bug](Report a Bug)

Other problems? See: [Troubleshooting](Troubleshooting)