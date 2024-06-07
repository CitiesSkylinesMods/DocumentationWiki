# Localisation Guidelines

> Verified: April 2020 (TM:PE 11.4.0)

We are hugely appreciative of anyone who can help us translate TM:PE in to other Languages.
See [](Adding-a-new-language.md).

[![Crowdin](https://badges.crowdin.net/tmpe/localized.svg)](https://crowdin.com/project/tmpe)

## Crowdin account

Before you can update translations, you'll need a user account on CrowdIn.

You can sign up, **for free**, here: [Crowdin Join](https://crowdin.com/join)

You can view and edit translations here: [TM:PE on Crowdin](https://crowdin.com/project/tmpe)

## Languages

Once your account is set up, navigate to the [TM:PE on Crowdin](https://crowdin.com/project/tmpe) to view the languages.

Your preferred languages (as defined in your user account) are donated with a ⭐️ icon and should appear at the top of the list, for example:

> [![TM:PE Languages](picCrowdin_languages.png)](https://crowdin.com/project/tmpe)
>  
> _If your language isn't listed yet, contact us via [Discord Chat](https://discord.gg/faKUnST) or leave a comment on the TM:PE workshop page._

Click a language to view its files...

## Language files

TM:PE translations are split into several language files, which look like this:

> ![TM:PE Language Files](picCrowdin_files.jpg)

The progress bar depicts the current status of each file:

* Green = Approved translations
* Blue = Pending approval
* Grey = Missing translations

Click a language file to display its strings...

## Translation strings

The translations strings are listed in the column on the left:

> ![TM:PE Strings](picCrowdin_strings.png)

The icons on the left show the status of each string:

* Red square with a dot = Not yet translated
* Green square = Translated, but not yet approved
* Check mark = Approved translation

Click on any string to show its detail screen:

> ![TM:PE String detail](picCrowdin_stringDetails.png)

In the top box you'll see the **Source string**, which is the **key** TM:PE uses to locate a translation.

Each source string includes a **prefix followed by a colon** - in the example above it's `Checkbox:`. Do NOT include the prefix in your translated string; you only need to translate the text _after_ the `:` - in the example above that would be `Ignore disabled mods`.

The **Context** section provides some additional detail about where the string is used, often with a screenshot. If you click a screenshot you'll see a red box depicting where the string is used.

Below the context panel, the current translation (if there is one) is shown. Add or edit the translation, then click the **Save** button to submit it for approval.

> You may see some on-screen warnings when saving, like this:
> ![TM:PE Save warning](picCrowdin_saveWarning.png)  
> Ignore them and click the "Save Anyway" button.

After saving a string, you'll automatically be taken to the next untranslated string in the current file.

_Our team will get notified of any new or changed translations and will review them. Once approved, your translations will go in to TM:PE and will be published with the next update to the workshop page._

## Selecting a different language file

If you've finished making changes in a file and want to switch to another file, click the button in the top-left corner of the screen:

> ![TM:PE Menu button](picCrowdin_hamburgerMenu.jpg)

You'll see a menu like this:

> ![TM:PE Menu](picCrowdin_changeLanguage.jpg)

Then click "Open..." and you'll get the list of Language files again.

## See also

[](Settings.md):

* [](General.md) - select language to use

[](Contributing.md):

* [](Priority-Signs-Icon-Themes.md) - localise UI for [](Priority-Signs.md)
* [](Speed-Limit-Icon-Themes.md) - localise UI for [](Speed-Limits.md)
* [](Timed-Traffic-Light-Buttons.md) - localise UI for [](Timed-Traffic-Lights.md)

Old stuff:

* [](Localisation-(Old-Format).md) - no longer used, but retained for historians