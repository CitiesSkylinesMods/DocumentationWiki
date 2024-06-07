> Verified: November 2021 - TM:PE 11.5

# Symptom

![Screenshot](https://i.imgur.com/0sdm0AD.jpg)

* A large number of cims are stuck waiting to cross the road
* Note: Traffic jam in image above was unrelated (was just traffic lights on red)

# Cause

* A game limitation prevents distant sidewalks from being connected
    * The issue is most common on huge junctions caused by very large roads.
    * The issue may also arise if you make a junction too big when using Node Controller mods.
    * Asset creators: If your road asset creates junctions that are `64f` or bigger, it will cause this problem.
* There are potentially some other causes which are still being investigated (see [Issue #1110](https://github.com/CitiesSkylinesMods/TMPE/issues/1110)).

# Solution

* Make the junction smaller:
    * Use smaller roads if possible, and avoid sharp angles which can sometimes cause large junctions
    * Use [Node Controller](https://steamcommunity.com/sharedfiles/filedetails/?id=2472062376) mod to shrink the size of the junction
* Make a bridge or tunnel:
    * Use pedestrian path networks to create a bridge/tunnel
    * [Automatic Pedestrian Bridge Builder](https://steamcommunity.com/sharedfiles/filedetails/?id=2030755273) mod makes it easy to add bridges (and tunnels!) at junctions
* Disable crosswalks that are causing problems
    * Use [Junction Restrictions](Junction Restrictions) tool to disable the crosswalks
* Check for broken nodes, etc.
    * Use the [Broken Nodes Detector](https://steamcommunity.com/sharedfiles/filedetails/?id=1777173984&searchtext=broken+nodes+detector) mod to scan for and fix some common road problems.
    * See guide: [How to remove ghost nodes and broken nodes](How to remove ghost nodes and broken nodes)
* Try to "free" the cims:
    * Click **Reset stuck cims and vehicles** button in [Settings](Settings) [Maintenance](Maintenance).

# Fixed?

If not, please let us know in [Issue #1110](https://github.com/CitiesSkylinesMods/TMPE/issues/1110).

Other problems? See: [Troubleshooting](Troubleshooting)