# Cims are Waiting for Taxi in Middle of Road
## Symptom

* Cims stand in middle of a road (or some other strange location) waiting for taxi

![Screenshot](https://i.imgur.com/0RhSqvL.png)

## Cause

* Building asset defines a Taxi de/spawn points in wrong place
* Building asset doesn't define a Taxi de/spawn point and the game creates one in wrong place

## Solution

Use [Building Spawn Points](https://steamcommunity.com/sharedfiles/filedetails/?id=2511258910) mod to check the spawn point for **Taxi** on nearby buildings. One of them probably has it in a weird location, or doesn't define it at all (in which case game will create one automatically, sometimes in weird location).

If you can find the problem building, add or move the de/spawn marker, eg. on the pavement or a driveway/parking area in the building. Note that it will only fix that specific instance of that building - but there's a button in the mod UI that updates all other instances of that building which can save some time.

## Was it Fixed?

If not, there's not much we can do about it, sorry.

Other issues? See [](Troubleshooting.md)