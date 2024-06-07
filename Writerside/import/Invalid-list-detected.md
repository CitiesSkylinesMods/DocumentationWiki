> Verified: February 2020

## Symptom

In the log file (and maybe on-screen), you see the following error:

* `Invalid list detected!`

In the full stack trace, which can be found in game log file, it's possible you also see:

* `at EightyOne.ResourceManagers ...`

## Cause

This error is a side-effect of other errors caused some game-breaking mods:

* **[Building Anarchy](https://steamcommunity.com/sharedfiles/filedetails/?id=912329352)**
* **[Terraform Tool 0.9](https://steamcommunity.com/sharedfiles/filedetails/?id=411095553)**
* **[Terrain Generator](https://steamcommunity.com/sharedfiles/filedetails/?id=453425585)**

If you see `at EightyOne.ResourceManagers` in the error stack trace, it could be that one of the mods above isn't compatible with 81 Tiles mod.

## Solution

Solve the root cause: [Array Index - Symptom 10](Array Index - Symptom 10)

## Fixed?

If not, you'll have to google, sorry.

Other issues? See: [Troubleshooting](Troubleshooting)