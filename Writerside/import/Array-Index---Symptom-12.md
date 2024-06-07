> Article verified: February 2020

> This is one cause of the [Simulation error Array index is out of range](Simulation error Array index is out of range) error.

## Symptom

You will see this error:

* `Simulation error: Array index is out of range.`

In the [**log file**](./Share-your-Cities-Skylines-log-file), you'll see one of the following below the error:

* `at GeneratedScrollPanel.IntializeUIAssetFilters`

You might notice issues like this in the build menus (particularly healthcare):

![Healthcare panel issue](https://imgur.com/ewfD7i8.png)

## Cause

This error is known to be caused by the [Nursing Homes for Senior Citizens](https://steamcommunity.com/sharedfiles/filedetails/?id=554232266) mod, which also sometimes causes game-breaking [[System.StackOverflowException]] errors.

> ![debug image](https://imgur.com/PNBn2aC.png)
> Image taken from dnSpy debugger while tracking down source of array index error

See also: [BoostHungry/SeniorCitizenCenterMod/issues/2](https://github.com/BoostHungry/SeniorCitizenCenterMod/issues/2)

## Solution

* Unsubscribe the [Nursing Homes for Senior Citizens](https://steamcommunity.com/sharedfiles/filedetails/?id=554232266) mod
* Unsubscribe any assets it uses (retirement homes, nursing homes, hospice, etc)
* Exit to desktop then restart the game

## Fixed?

If not, see other causes of [Simulation error Array index is out of range](Simulation error Array index is out of range).

Other issues? See: [Troubleshooting](Troubleshooting)