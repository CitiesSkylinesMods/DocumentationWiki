> Verified: February 2020

## Symptom

This error occurs late in the loading process or just after a city finishes loading:

* `FormatException: Invalid Image Format: failed to load`

In the full stack trace, which can be found in the log file, you might see one or more of these:

* `AssetIcons.IconModifier.PatchIcons`
* `AssetIcons.IconModifier.OnLevelLoaded`

## Cause

This is caused by either of the following mods:

* [Improved Asset Icons](https://steamcommunity.com/sharedfiles/filedetails/?id=508195208)
* [Improved Asset Icons (alternative)](https://steamcommunity.com/sharedfiles/filedetails/?id=747836519)

Those mods also cause [Object reference not set to an instance of an object](Object reference not set to an instance of an object) errors.

## Solution

Completely unsubscribe the mods listed above - they are game breaking.

If you need a better alternative, we recommend [Find It](https://steamcommunity.com/sharedfiles/filedetails/?id=837734529) mod which is extrmely reliable.

## Fixed?

If not, let us know - currently the mods above are the only _known_ causes of the error but it's possible there are other mods that cause it too.

Other issues? See: [Troubleshooting](Troubleshooting)