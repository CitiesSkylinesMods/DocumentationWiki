> Verified: January 2022

> This is one cause of the [Simulation error Array index is out of range](Simulation error Array index is out of range) error.

## Symptom

You will see this error, or similar, on screen and in the log file:

* `Simulation error: Array index is out of range.`

In the [**log file**](Share-your-Cities-Skylines-log-file.) search to see if you find this error (it could be anywhere in the log):

> Note: This error will only appear if you have TM:PE subscribed and it detected a ghost node. Even if you don't see the error, try the solution below regardless ;)

* `Node is not connected to segment`

The full error might look like this (`#` just denotes a number which isn't important):

* `Warning #: ExtSegmentEndManager.GetIndex(#, #): Node is not connected to segment.`

## Cause

This is due to **Ghost nodes** that aren't connected to any road/rail/path segments.

Usually these should not exist, however sometimes they occur due to reasons such as:

* Corrupted save game
* Missing network asset
* Mods that replace network assets
* Mods that alter road placement
* Mods that provide non-standard bulldozer tools

As long as the ghost node exists, you will likely get array index errors as the game and other mods break due to the faulty node.

## Solution

1. Subscribe and enable [Broken Nodes Detector](https://steamcommunity.com/sharedfiles/filedetails/?id=1777173984) mod.
2. Load your save
3. Open Broken Nodes Detector window with `Ctrl+0` (zero)
4. Run the various tests to detect and resolve issues.

That should clear away any ghost nodes.

## Fixed?

If not, see other causes of [Simulation error Array index is out of range](Simulation error Array index is out of range).

Other issues? See: [Troubleshooting](Troubleshooting)