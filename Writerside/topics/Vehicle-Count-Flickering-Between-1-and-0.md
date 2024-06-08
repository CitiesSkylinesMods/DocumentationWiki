# Vehicle Count Flickering Between 1 and 0

> Verified: January 2022 - TM:PE 11.5.2 / TM:PE 11.6

## Symptoms

* When clicking a service building, the info panel shows vehicle count flickering between 0 and 1.
* Sometimes you'll see vehicles temporarily spawn then despawn

## Causes

Common causes include:

1. Broken road connections (vehicle can't reach destination)
2. Reached the PathUnit limit (game limit of vehicle routes)

## Solutions

1. To find broken road connections:
    * If you're using [No Problem Notifications](https://steamcommunity.com/sharedfiles/filedetails/?id=917543381) mod,
      or similar, it might be hiding "No Road Access" problem notifications:
        * Make sure it isn't hiding `RoadNotConnectedProblem` (if in doubt, disable the mod, exit to desktop, then
          reload your city)
    * Subscribe and
      enable  [Check Road Access for Growables](https://steamcommunity.com/sharedfiles/filedetails/?id=2454302667) (`CRAFG`),
      then use it to check your city
        * Look for any "Road Not Connected" notifications over buildings and fix those issues
        * Just repositioning the building will usually solve the issue
        * If using Move It mod, note that the building must be facing the road (when placing roads, you'll see arrows on
          buildings indicating the front of the building)
    * Subscribe and
      enable [Broken Nodes Detector](https://steamcommunity.com/sharedfiles/filedetails/?id=1777173984) (`BND`), then
      use it to check your city
        * Use its "Disconnected Buildings" button to cycle through buildings with the problem, and fix each one
        * Note that the building might not have a notification icon over it as other notifications (no water, etc.) have
          higher priority than "No Road Access"
        * After fixing buildings, run both `CRAFG` and `BNG` tests again to check that there are no broken road
          connections remaining
2. To increase the PathUnit limit:
    * The [More PathUnits](https://steamcommunity.com/sharedfiles/filedetails/?id=2710657019) mod can increase the game
      limit, but read the description on the workshop page carefully! Once you use this mod, your city will not be able
      to load without it.

## Was it Fixed?

If not, try these guides:

* [](Hearses-not-spawning.md)
* [](Vehicles-not-spawning.md)

Other issues? See: [](Troubleshooting.md)