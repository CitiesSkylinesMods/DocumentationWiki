# Lane Arrows and Connectors not Loading

## Symptom

* [#1146](https://github.com/CitiesSkylinesMods/TMPE/issues/1146) After loading a city, it looks like the lane
  connectors / arrows haven't been restored.

## Cause

For technical reasons, TM:PE waits until after the first simulation step has completed before it updates certain
customizations.

If the game is "Paused on load", the first simulation step won't complete until _after_ you unpause the game.

## Solution

* Unpause the game so the first simulation step can complete.
* Additionally, check you have [](Lane-Connectors.md) enabled in [](Maintenance.md) in [](Settings.md)

Note also that some roads don't include lane arrow decals (or don't have a full set of lane arrows) so there might not
be any visual indicator of the lane arrows loading.

## Was it Fixed?

If not, please let us know!

Other issues? See: [](Troubleshooting.md)