> Verified: March 2022 - TM:PE 11.6.5.2

## Symptom

* After loading your city, you notice that the terrain and roadside grass has turned white.

## Causes

This issue is _not_ caused by TM:PE.

Two known causes are:

* Broken or incompatible mods
* Theme Mixer 2: A required theme has been unsubscribed or removed from workshop.

## Solution

The best way to check for broken or incompatible mods is to use the [Compatibility Report](https://steamcommunity.com/sharedfiles/filedetails/?id=2633433869) mod - launch `Cities.exe` and then review the report to see if any of your mods are known to cause the problem.

If you suspect it's a Theme Mixer issue, you'll need to locate your theme mix files. On Windows, they are usually located in:

```batch
C:\Users\<Username>\AppData\Local\Colossal Order\Cities_Skylines\Addons\Mods\<ThemeName>
```

_Where `<UserName>` is your windows username (or part of it) and `<ThemeName>` is the name of your theme mix._

Open the `UsedAssets.txt` file - it contains a list of themes that are required for your theme mix.

Inside the file you'll see something like this:

```js
Themes:
921636136.Springwood
828037844.Farmland
1566764377.Athenian Theme
1196125311.Sedona
1447046893.Aiguille Verte
```

The number at the start of each line is the Workshop ID of the theme. Put that in the following URL to visit the workshop page to see if it still exists:

```batch
https://steamcommunity.com/sharedfiles/filedetails/?id=<WorkshopID>
```

For example: https://steamcommunity.com/sharedfiles/filedetails/?id=1566764377

In the URL above, I found that the `Athenian Theme` theme (id: `1566764377`) had been removed from the workshop - and that's why I'm getting white grass textures.

Next, work out which specific theme mix elements are affected by the missing theme. In the same folder that contains `UsedAssets.txt`, you'll find another file called `ThemeMix.xml` - open that file, then search for the numeric ID, and you'll be able to determine which theme elements are affected. In my case it was only the `Grass Diffuse Texture` which used textures from that theme.

To resolve the issue, load your city, open Theme Mixer 2 panel, then navigate to the affected elements and update them to use another theme.

## Fixed?
