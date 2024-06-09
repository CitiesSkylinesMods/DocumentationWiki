# Array Index - Symptom 10

> Article verified: February 2020

> This is one cause of the [](Simulation-error-Array-index-is-out-of-range.md) error.

## Symptom

You will see this error:

* `Simulation error: Array index is out of range.`

In the [**log file**](Share-your-Cities-Skylines-log-file.md), you'll see one of the following below the error:

* `at GeneratedScrollPanel.IntializeUIAssetFilters`

You might notice issues like this in the build menus (particularly healthcare):

![Healthcare panel issue](picHealthCare_bug.png)

## Cause

This error is known to be caused by
the [Nursing Homes for Senior Citizens](https://steamcommunity.com/sharedfiles/filedetails/?id=554232266) mod, which
also sometimes causes game-breaking [[System.StackOverflowException]] errors.

![debug image](picHealthCare_debug.png){style="block"}
_Image taken from dnSpy debugger while tracking down source of array index error_

See also: [BoostHungry/SeniorCitizenCenterMod/issues/2](https://github.com/BoostHungry/SeniorCitizenCenterMod/issues/2)

## Solution

* Unsubscribe the [Nursing Homes for Senior Citizens](https://steamcommunity.com/sharedfiles/filedetails/?id=554232266)
  mod
* Unsubscribe any assets it uses (retirement homes, nursing homes, hospice, etc.)
* Exit to desktop then restart the game

## Was it Fixed?

If not, see other causes of [](Simulation-error-Array-index-is-out-of-range.md).

Other issues? See: [](Troubleshooting.md)