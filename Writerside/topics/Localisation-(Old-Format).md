# Old: Localisation Format

> # NOTE
> This is the old documentation that applies to **TM:PE v11.0-alpha6 and all earlier verisons**.
>
> **TM:PE v11.0-alpha7 and all later versions** use a completely new localisation system. For details on that,
> see [](Localisation.md).

----

We are hugely appreciative of anyone who can help us translate TM:PE in to other [](Languages.md).

## Where to find the localisation files

Localization `.txt` files are located in
the [/TLM/TLM/Resources](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/tree/master/TLM/TLM/Resources)
folder.

Filenames for translations (except for English) have the format `lang_[id].txt` where `id` is
the [ISO 639-1 code](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) associated with your language.

For example, the code for Vietnamese is `vi` so the file would be `lang_vi.txt`. If there are dialects you can specify
those too; for example: `lang_zh-tw.txt` is language `zh` and dialect `tw`.

The English file, which is the default language and also the template to use for other languages,
is [`lang.txt`](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/blob/master/TLM/TLM/Resources/lang.txt).
See below for details of file format and how to send us your language files.

## File format

Take a look at some of the existing files for reference; they use `key value` pairs where the `key` and the `value` are
separated by a space, like this:

```
Switch_traffic_lights 信号の付け外し
Add_priority_signs 優先関係標識の追加
Manual_traffic_lights 信号の手動切替
```

In the sample above, `Switch_traffic_lights` is a `key`, and `信号の付け外し` is its `value` (translation).

Important:

* The `key` must be separated from the `value` by a space character
* Only the `value` (translation) should be changed, do not change the `key`
* Each `key value` pair must be on a single line in the file

Note: New lines within a `value` string are denoted with `\n` - you may need to change the position of these in some of
the longer `TMPE_TUTORIAL_BODY_...` translations to ensure correct layout.

When a language is selected in TM:PE, the mod looks for the `key` in the text file and, if found, it grabs whatever is
after the first space on that same line (the `value`) and shows that to the user.

### Updating an existing file

If you need to update an existing translation, to correct a mistake or complete missing translations, just edit the
existing file.

### Creating a new file (adding a new language)

Use
the [`lang.txt`](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/blob/master/TLM/TLM/Resources/lang.txt)
as a template - copy it and then rename it as specified above with the
appropriate [ISO 639-1 language id](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) (for example `lang_ja.txt`
for Japanese).

Once that is done, just edit the values as necessary.

> Note: Additional steps are required to complete the process of adding a new language. Usually, the TM:PE support team
> will perform those tasks. However, if you want to help with that too,
> see: [](Adding-a-new-language.md)

## Sending us your file(s)

If you are familiar with **GitHub**, send us a Pull Request to the `krzychu124 / master` branch. _This is our preferred
way of getting language files._

Alternatively, you can send it to us any of these ways:

* **Discord**: Drag-drop the file in the **# Issues** chat room
* **Steam**: Paste a URL to the file on our workshop page
* **GitHub Issue
  **: [Click here to create a translation issue](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/issues/new?labels=localisation%2C+triage&template=translation-update.md)
* [**Pastebin**](https://pastebin.com/), [**Gist**](https://gist.github.com/), or similar: Create a new paste and send
  us the URL. Make sure the site you use supports unicode (UTF-8 encoding) and also provides access to a "Raw" (
  text-only) view of the file.

We always credit contributors in our release notes. We will use whatever username you are using when you send us the
file - if you want a different name using, for example your Steam username, please let us know.