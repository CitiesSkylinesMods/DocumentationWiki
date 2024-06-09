# Simulation failed Deserialization tag mismatch

> Verified: April 2022 - TM:PE 11.6.5.2

## Symptoms

This error usually appears on the loading screen (if using Loading Screen Mod), or as an error popup after a city loads,
or in the game log.

![tag mismatch](picTagMismatchError.png)

The word in brackets (e.g. `VehicleManager`) may change depending on the root cause of the error.

## Causes

These errors are _not_ caused by TM:PE.

There are two known causes of the error:

* `VehiclesManager` - the city requires More Vehicles mod
* `AreasManager` (or something about Areas / Tiles) - 81 Tiles mod is missing, or corrupt data

## Solutions

If the error mentions `VehicleManager`:

* Subscribe and enable [More Vehicles](https://steamcommunity.com/sharedfiles/filedetails/?id=1764208250) mod
* The city should now load (so long as you don't have any mods that are incompatible with More Vehicles)

If the error mentions `Tiles` or `Areas` then it is likely an issue with 81 Tiles:

* Subscribe and enable [81 Tiles](https://steamcommunity.com/sharedfiles/filedetails/?id=576327847) mod
* Try loading the city - if you still get a tag mismatch, try the button in 81 Tiles mod options

In both cases, make sure you don't have any incompatible
mods: [Compatibility Report](https://steamcommunity.com/sharedfiles/filedetails/?id=2633433869)

(Thanks to BloodyPenguin, Dymanoid, AquilaSol and 夕林樱花Adonis for info about these errors)

## Was it Fixed?

If not, there's probably no way to recover the city, unless you have backups of older saves?

Other issues? See: [](Troubleshooting.md)