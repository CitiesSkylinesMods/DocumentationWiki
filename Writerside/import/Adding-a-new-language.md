> If you are a translator, please see: [Localisation](Localisation)

## Overview

This guide is primarily aimed at TM:PE support team who will ensure the new language is properly defined, but translators are more than welcome to go through these steps themselves if they feel comfortable doing so.

When adding a new language, the file must be embedded within the published TM:PE files (not just copied to the build folder) and the `Translation.cs` class must also be updated.

## Check filename and format

Common errors are:

* Invalid filename (should be `lang_*.txt`, where `*` is language code - eg. `es` or `zh-tw`, etc.)
* Actual line breaks within translation strings (use `\n` instead)
* Missing space between key and value
* Translated keys (they should all be in English)
* Missing keys - copy them over from `lang.txt`, including the English values; they can be translated later

See: [Localisation](Localisation) for full details.

## Embed the resource

The localisation file must be placed in `TLM/TLM/Resources` folder, where all the existing `lang_*.txt` files are.

Open Visual Studio and under the `TLM` project, find and right-click the `Resources` folder then choose `Add existing item...`:

![Add to resources](https://user-images.githubusercontent.com/1386719/58388665-9b53aa00-8019-11e9-8863-bb8a528106a1.png)

Locate the new file (you might need to set file types to `All Files` in the file dialog) and add it.

Once added:

* Right-click the file in the sidebar (eg. `lang_es.txt`)
* Choose `Properties...`
* Make sure `Build Action` is set to `Embedded Resource`

![Embed as resource](https://user-images.githubusercontent.com/1386719/58388698-f08fbb80-8019-11e9-9834-d7eb6c25533e.png)

## Edit `Translation.cs` class

Open the [`TLM/TLM/UI/Translation.cs`](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/blob/master/TLM/TLM/UI/Translation.cs) file in Visual Studio and locate the `Translation()` constructor.

You will see two lists being populated, both need updating to include the new language.

> Note: For ease of maintenance, the lists are sorted by language code, so insert or append the new language as applicable.

Add the language code, for example if the filename is `lang_es.txt` you'd add:

```csharp
AVAILABLE_LANGUAGE_CODES.Add("es");
```

Then add the label that will appear in the drop-down language select list in [General](General) [Settings](Settings), for example:

```csharp
LANGUAGE_LABELS["es"] = "Español";
```

As you can see the label should be the translated name of the language.

## Test it's working

* Save your changes, then build the project (`Ctrl` + `Shift` + `B`). For more info, see:
    * [Building from Source](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/blob/master/TLM/BUILDING_INSTRUCTIONS.md)
    * [Building from Pull Requests](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/blob/master/TLM/PR_REVIEW_INSTRUCTIONS.md)
* Launch C:SL and make sure the local version of the mod is enabled (unsubscribe any other versions)
* Start a new game, and then go in to TM:PE mod options and change the language.
* In particular, test:
    * Text in the mod options - make sure no overlaps
    * Tool tips on the [Toolbar](Toolbar)
    * Text in the [Traffic Lights](Traffic Lights) editor window
    * Help popups (with a TM:PE tool active, click the games' `?` advisor button)

If it all looks good, submit a PR (or commit to the existing PR) ready for code review.

Remember to update the [Languages](Languages) page in the wiki after the PR is merged.