> Verified: April 2022 - TM:PE 11.6.5.2

# Symptom

* Text missing from user interface (eg. no content in timed traffic lights panel)

# Cause

* [#301](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/issues/301): Missing fonts

# Solution

This issue seems most common on Linux distros with non-standard font mappings.

Find out which font the game is using and ensure it (or an alias to an alternative) exists on your machine. The game should bundle its own fonts, listed below:

> ![fonts](https://user-images.githubusercontent.com/1386719/57154425-bd6a5b80-6dd0-11e9-8a1f-2519b58dc8e0.jpg)

Alternatively, you can change the font with one of these mods:

* [Font Selector](https://steamcommunity.com/sharedfiles/filedetails/?id=412149127) (last checked: April 2009)
* [Skylines Font](https://steamcommunity.com/sharedfiles/filedetails/?id=408286108) (seems to work, but Font Selector might be easier to use)

# Fixed?

If not, it could be caused by other issues such as:

* [Clicking button makes text dissapear](Clicking button makes text dissapear)
* [Road names distorted](Road names distorted)

Other issues? See: [Troubleshooting](Troubleshooting)