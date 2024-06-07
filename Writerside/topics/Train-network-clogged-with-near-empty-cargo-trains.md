# Train Network Clogged With Cargo Trains

## Symptom

Train network is clogged up with nearly empty cargo trains

## Cause

This can happen when trains are unable to leave cargo stations.

## Solution

First, check that your rail network is properly configured. You should make use of "Stop" signs at junctions and, in some cases, also near the X-connections either side of cargo stations:

* You need to ensure trains leaving the station have priority, as that will free up space for any train wanting to enter the station.
* So, a Stop sign should be placed facing the entrance to the station (NOT the exit from the station).

Second, it is always a good idea to separate your cargo and passenger train networks to reduce changes of congestion and train jams:

* If you have TM:PE, you can use [Vehicle Restrictions](Vehicle-Restrictions.md) on the train tracks to control what type of train can use the tracks.
* Alternatively, see [this Steam Guide](https://steamcommunity.com/sharedfiles/filedetails/?id=564699396) for some ways to achieve similar results in the vanilla game.

Third, make sure you haven't altered the train tracks in the station with Move It mod - this can confuse the AIs which don't always register changes to station tracks, particularly if you only changed the length of the station tracks:

* One confirmed case of this was caused by selecting the station and the tracks with Move it, then moving the station.
* One end (node) of the station tracks moved with the station, while the other end remained fixed to the rail network outside the station.
* This caused the station tracks to be stretched, but in such a way that the game only registered the station being moved but not the tracks being altered.

If you have broken station tracks, you can try fixing as follows (thanks to **tenderloveheart** for this solution):

* Bulldoze the broken tracks
    * To bulldoze station tracks, hold **Alt** key then select one of the nodes with Move it, then use Move it bulldozer tool to delete the node (track segments either side will be deleted).
* Click the station to open its info panel
* Use the "Move building" button and relocate the station somewhere else
* Then rebuild the station tracks and connect to your network

If that fails, bulldoze the station completely (including any station tracks that might remain after bulldozing the building), save them game, exit to desktop. That will make the game forget you ever had that station. Reload Cities: Skylines and then load your save game. Finally, build a new station.

If you are still suffering from nearly empty cargo trains, try the **[Cargo Hold Fix](https://steamcommunity.com/sharedfiles/filedetails/?id=1721492498)** mod. It makes cargo trains wait longer so they fill up more. A side effect is that you will also need fewer cargo trains.

## Fixed

If not, see: [Public Transport, and cargo Trains](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/wiki/Troubleshooting#public-transport-and-cargo-trains)

Other issues? See: [Troubleshooting](Troubleshooting)