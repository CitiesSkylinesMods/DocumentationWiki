# Intercity Buses not Working
> Verified: January 2022 - TM:PE 11.5.2 / 11.6

## Symptom

Intercity buses were introduced with the Sunset Harbor update, but some users report:

* No intercity buses arriving in the city, or
* Intercity buses not using some outside connections, or
* Cims not using intercity buses

## Causes

* No intercity bus station/terminal in the city
* Roads with zoning can't be used for outside connections
* Roads without hidden 'outside connection' flag won't work as outside connections
* [#960](https://github.com/CitiesSkylinesMods/TMPE/issues/960): Vanilla game bug prevents intercity buses entering from 2-way roads
* 81 Tiles mod breaks intercity bus stops/stations/terminals outside central 25 tile area

## Solutions

* Make sure you have at least one intercity bus station/terminal in your city
    * You can make normal bus stations/terminals accept intercity buses with the [Intercity Bus Control](https://steamcommunity.com/sharedfiles/filedetails/?id=2499771767) mod
    * Detailers might like this individual intercity bus stop asset: [Intercity Bus Stop](https://steamcommunity.com/sharedfiles/filedetails/?id=2049510825)
* Make sure your outside connections are valid:
    * See: [](Outside-connections-not-working.md)
* Intercity buses cannot enter via 2-way road outside connections
    * There is currently no way to make intercity buses use 2-way outside connections
    * You'll need at least one 1-way outside connection (both entering and leaving the city)
* Some roads don't allow the game to add virtual bus lane
    * Using normal 1-way vanilla highway (both entering and leaving the city) should get you a working route
* 81 Tiles mod doesn't support intercity bus stops/stations/terminals outside central 25 tile area
    * Cims won't use the buses outside central 25 tiles
    * No solution currently, although Quistar is working on new 81 Tiles mod as part of Extended Managers Library mod.

## Was it Fixed?

If not, please let us know.

Other issues? See: [](Troubleshooting.md)