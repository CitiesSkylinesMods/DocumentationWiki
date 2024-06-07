> Verified: January 2022 - TM:PE 11.5.2 / TM:PE 11.6.3

> Note: This may merit some simplification in future as we now have multiple changelogs happening which is messy.

## `CHANGELOG.md`

The main changelog is located in the repo at: https://github.com/CitiesSkylinesMods/TMPE/blob/master/CHANGELOG.md

The badges and their links which appear at the top are automatically updated so you don't need to change those. The `Legend` section only needs updating when a new workshop page is created to provide some brief details of the history of the mod.

The heading format is important because `What's New` panel can link to them. Example below:

```
#### TM:PE V[11.4.0](https://github.com/CitiesSkylinesMods/TMPE/compare/11.3.2...11.4.0) STABLE, 22/05/2020
```

The resulting anchor link to a heading (when you hover mouse over the rendered markdown) should look something like:

```
#tmpe-v1140-stable-22052020
```

The general sequence of entries should be:

* Added
* Fixed
* Updated
* Removed
* Meta (if applicable)
* Steam (link to the workshop page of the release)

## `README.md`

Again, this has some badges at top, most of which automatically update. However, you'll need to update the game version badge manually each time CO/PDX release a new DLC or CCP.

```html
<a href="https://store.steampowered.com/app/255710/Cities_Skylines/"><img src="https://img.shields.io/static/v1?label=cities:%20skylines&message=v1.13.0-f8&color=01ABF8&logo=unity" /></a>
```

In the HTML above, update the version as applicable (it's showing version `v1.13.0-f8` in the example above).

The page also contains release notes for the most recent `STABLE` and `TEST` releases - these can be copy pasted from `CHANGELOG.md`.

## What's New panel

> This is a recently introduced feature and is subject to ongoing change, eg. see [Issue #1288](https://github.com/CitiesSkylinesMods/TMPE/issues/1288).

A curated changelog is displayed in-game whenever the mod is updated. The details are pulled from the `whats_new.txt` resource in the `TLM/TLM/Resources` folder.

Each release has a `[Version] ... [/Version]` block in the file, for example:

```
[Version] 11.6.1.3
[Released] October 14th 2021
[Link] tmpe-v1161-test-14102021
[Fixed] Cannot setup timed traffic lights on monorail nodes #1160
[Updated] Performance, memory efficiency #1161 #1162 #1164 #1165 (thanks Egi)
[Updated] ...
[/Version]
```

The tags are:

* `[Version]` - postfix the mod version number (see above for example)
    * This appears in purple panel in the UI
* `[Stable]` - this keyword indicates a version has been released to STABLE workshop page
    * In STABLE releases, only the `[Stable]` versions are displayed (others hidden)
* `[Released]` - postfix the release date (month day year)
    * This appears next to the version number in the UI
* `[Link]` (optional) - the anchor link (excluding `#`) for the `CHANGELOG.md` file as discussed earlier on this page
    * If present, the date shown in UI will be hyperlinked to the changelog
* Changelog items (there can be zero or more of each of these):
    * `[New]` (green lozenge in UI) - for new features or major overhauls (eg. rewrite of speed limits UI)
    * `[Mod]` (amber lozenge in UI) - anything relating to other mods (eg. marked (in)compatible, etc.)
    * `[Fixed]` (blue lozenge in UI) - bug fixes or other resolved issues
    * `[Updated]` (blue lozenge in UI) - an existing feature was updated (eg. to improve performance etc.)
    * `[Removed]` (red lozenge in UI) - when obsolete code/feature is removed
    * Note: Changelog items are autoamtically sorted in to the order shown above
* `[/Version]` - must appear at end of each version block

The [`TMPE.log`](TMPE.log) file will detail any errors in the parsing process (you'll usually see an error on the main menu screen as well).