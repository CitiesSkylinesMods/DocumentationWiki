## Symptom

When the Electricity or Water build menus are open, the power lines or water pipes are not highlighted on the map.

## Cause

There are several known causes of this issue:

1. Mods which prevent automatic info view display when a build menu are open
2. Mods that remove need for powerlines and/or water pipes
3. Skipping vanilla assets for powerlines and/or water pipes using Loading Screen Mod `skip.txt`
4. Custom assets, if used, might be missing

## Solution

Check to see if you have mods that disable automatic info views:

* [Toggleable Whiteness](https://steamcommunity.com/sharedfiles/filedetails/?id=465318661) - this mod is designed to prevent automatic info view (white map and buildings) display; it affects all build menus including Electricity, Water, Parks, Education, etc.
    * After opening a build menu, manually open the relevant info view
    * Alternatively disalbe or unsubscribe the mod if you want info views to be shown automatically
* [Toggle It](https://steamcommunity.com/sharedfiles/filedetails/?id=1764637396) - this mod has a button that can toggle whether the automatic info view is displayed when a build menu is opened
    * After opening a build menu, either manually open the info view or click the button that toggles the automatic info view

Check for mods that remove the need for powerlines or pipes (savegames from Steam Workshop often use these mods so the city creator doesn't need to add powerlines and/or pipes):

* [Remove Need For Pipes](https://steamcommunity.com/sharedfiles/filedetails/?id=576997275)
* [Remove Need For Power Lines](https://steamcommunity.com/sharedfiles/filedetails/?id=572888650)
* [Electric Roads Mod](https://steamcommunity.com/sharedfiles/filedetails/?id=1689984220)

If you use [Loading Screen Mod](https://steamcommunity.com/sharedfiles/filedetails/?id=667342976) (recommended for all users!), make sure you've [not skipped](https://steamcommunity.com/workshop/filedetails/discussion/667342976/1741105805762370419/) the following assets:

* `Electricity Pole`
* `Water Pipe Junction`
* `Heating Pipe Junction`

Finally, if you are using custom assets, make sure they are:

* Subscribed and visible in Main Menu > Content Manager > Assets
* Enabled in Main Menu > Contnet Manager > Assets screen

## Fixed?

If not, ask for assistance in discussion forums.

* If you find a reason for missing pipes/powerlines not mentioned above, please let us know so we can add to the list.

Other issues? See: [Troubleshooting](Troubleshooting)