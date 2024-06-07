> Verified: April 2022 - TM:PE 11.6.5.2

## Symptom

One or more of these issues:

* Vehicles floating to car parking spaces
* Vehicles floating randomly across the map
* Cims walking long distance over terrain (not on a path)

> There is a similar issue that affects cyclists/bikes: [Floating cyclists and discarded bicycles](Floating cyclists and discarded bicycles)

## Cause

Vehicles floating to car parking spaces is due to the Parking AI in vanilla game. Note that TMPE's parking AI is also based on the vanilla AI and suffers the same issue. There is currently no solution for that issue but we are investigating to see if there's a way to reduce it.

Vehicles floating randomly across the map is likley due to mods such as Service Vehicle Selector, particularly if they are floating to/from cargo or transport hubs ([example](https://steamcommunity.com/app/255710/discussions/0/3949028823313156915/)).

If it's cims (pedestrians) walking long distance over land (not paths or roads), we do not currently know what causes that. It is possibly related to tourists trying to leave the city if their vehicle has despawned or if they can't find public transport, but that's not confirmed yet.

## Solution

To reduce cars floating to car parks, try moving car park to different side of road or a differnet road entirely. Note that vehicles drive to destination and _only then_ do they look for parking. If parking is within certain rage they just float in a straight line to the parking space.

For vehicles floating around cargo and transit hubs, try unsubscribing Service Vehicle Selector or similar mods, then exit to desktop (flush the mod from RAM) and reload your save to see if that fixes it.

For cims walking across the map, ensure there are public transit hubs that link to outside connections as tourists will use that if they can no longer find or reach their car.

## Fixed?

If not, try disabling various mods and workshop vehicles to see if that helps (if you find bugged mods or vehicles, please let us know so we can add to the list).

Other issues? See: [Troubleshooting](Troubleshooting)