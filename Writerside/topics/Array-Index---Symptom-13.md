> Verified: February 2020 - TM:PE 11.1.1

> This is one cause of the [Simulation error Array index is out of range](Simulation error Array index is out of range) error.

## Symptom

You will see this error:

* `Simulation error: Array index is out of range.`

In the [**log file**](Share-your-Cities-Skylines-log-file.), you'll see one of the following below the error:

* `at TransportLineAI.CheckNodePosition ...`

## Cause

This happens when a stop on a transport line is broken due to missing network assets (roads, rails, etc); the game can't chance the position because the road or track no longer exists.

## Solution

If you haven't already done so, subscribe and enable [Loading Screen Mod](https://steamcommunity.com/sharedfiles/filedetails/?id=667342976) (LSM). In it's mod options, enable sharing/optimisation features.

The first thing we need to deal with is the missing networks. You have two choices - either try and revive them, or just get rid of them...

#### To _revive_ missing networks

* In LSM mod options, enable the [**Asset Reporting** options](https://steamcommunity.com/sharedfiles/filedetails/?id=1846793796)
* Load your city
* When it loads, exit game to desktop
* Look in the LSM reports and it will list the missing networks - resubscribe them

#### To _remove_ missing networks

* In LSM mod options, enable the [**Safe Mode** options](https://steamcommunity.com/workshop/filedetails/discussion/667342976/1626286205707786286/)
* Load your city
* When it loads, save it under a new file name
* Once saved, exit game to desktop

You should now be able to load that new save game without too many errors.

#### Remove broken transport lines

After sorting out the missing networks, you will probably still have some broken transport lines that need removing:

* Subscribe and enable [Broken Nodes Detector](https://steamcommunity.com/sharedfiles/filedetails/?id=1777173984) mod
* Load your city
* In-game, press **Ctrl + Zero** (or **Cmd + Zero** on Macs)
* Use each of the tools:
    * **Detect disconnected PT stops** (repeat process until it's not finding any more)
    * **Remove ghost nodes**
    * **Run detector** (if it finds anything, move or bulldoze the pinned road/track/path)
* Now save your game under a new file name
* Once saved, exit game to desktop

Next time you load up, just to be extra careful, use the process listed in **To _remove_ missing networks** section above.

## Fixed?

If you still get the array index error shown in **Symptoms** section above, it could be some other cause of broken transport routes. You'll have to ask for help in the Steam forums, reddit, discord servers, etc.

Other issues? See: [Troubleshooting](Troubleshooting)