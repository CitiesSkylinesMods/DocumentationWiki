> Article verified: January 2022

# Symptom

* When I bulldoze or alter a road, cars that were just about to drive on to it despawn instead of finding a different route

# Cause

There were two bugs in TM:PE versions 1.10.17 and earlier:

* [#86](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/issues/86): Delete a road and vehicles despawn rather than reroute
* [#218](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/issues/218): Deleting, upgrading, or otherwise updating a road makes vehicles despawn instead of recalculating their route

There is also a bug in the vanilla game:

* [#277](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/issues/277): "Vibrating nodes" vanilla bug causes traffic to despawn

# Solution

1. Make sure you are using the latest version of TM:PE (must be at least v10.18 or later).
2. Ensure you only have one copy of TM:PE subscribed (don't just disable other versions, completely unsubscribe them)
3. Remove any broken nodes. See: [How to remove ghost nodes and broken nodes](How to remove ghost nodes and broken nodes).

# Fixed?

If not, please let us know: [Report a Bug](Report a Bug)

Other problems? See: [Troubleshooting](Troubleshooting)