# Share Log File

> Verified: February 2022 - TM:PE 11.6.4.7

> ⚠️ **Check the Compatibility Report first**
>
> About 50% of the error reports we get are due to old / broken / incompatible mods.
> The [Compatibility Report](https://steamcommunity.com/sharedfiles/filedetails/?id=2633433869) mod is the fastest way to
> find known problems with your mods - it's a collaboration between end-users and mod developers to help navigate the vast
> array of mods that are out there.

## Why we need the log file

The log file contains detailed information about any errors that have occurred, and that helps us determine where to
look in the code as a starting point in our bug-fixing investigations.

> Details of how to share log file are posted near end of this page.

## Log file names

We always need the game log as it contains hardware details and detailed error reports:

* `output_log.txt` (Windows)
* `Player.log` (Mac / Linux)

We also need:

* `TMPE.log` - usually in same folder as game log (see [[TMPE.log]] for details)

## Log file locations

Location depends on operating system...

### Windows:

The game log is called **`output_log.txt`**. Location depends on the game portal you use to play the game (click portal
name below to show paths):

<ul>
<li><details><summary><b>Steam</b></summary>

```shell
<SteamFolder>\SteamApps\common\Cities_Skylines\Cities_Data\output_log.txt
```

_The `<SteamFolder>` is _usually_ found at `C:\Program Files (x86)\Steam`._
</details></li>

<li><details><summary><b>Epic</b></summary>

```shell
<EpicFolder>\CitiesSkylines\Cities_Data\output_log.txt
```

_The `<EpicFolder>` is _usually_ found at either `C:\Epic Games` or `C:\Program Files\Epic Games`
or `C:\Program Files (x86)\Epic Games`._
</details></li>

<li><details><summary><b>EA Origin</b></summary>

```shell
<OriginFolder>\CitiesSkylines\Cities_Data\output_log.txt
```

_The `<OriginFolder>` is _usually_ found at `C:\Program Files(x86)\Origin Games`._
</details></li>
</ul>

### Apple Mac:

The game log is called **`Player.log`** and can be found at:

```shell
Users/<username>/Library/Logs/Unity/Player.log
```

_The `<username>` folder is normally your login name._

### Linux:

The game log is called **`Player.log`** and can be found at:

```shell
~/.config/unity3d/Colossal Order/Cities: Skylines/Player.log
```

### Custom location

The location of the log file can be changed with
the `-LogFile` [launch option](https://steamcommunity.com/sharedfiles/filedetails/?id=466981085) (standard Unity
feature). The `TMPE.log` will be also placed in the same folder.

> Mod developers: See [PR #1151](https://github.com/CitiesSkylinesMods/TMPE/pull/1151) for how we did that.

## Obtaining list of mods

* If using **TM:PE v11-alpha3 or above**, a list of mods can be found in your [`TMPE.log`](TMPE.log.md) file. In the list,
  an asterisk (`*`) denotes enabled mods and exclamation marks (`!`) denote mods which are known to be incompatible with
  TM:PE.
* If using **TM:PE v10.21.1 or earlier**, subscribe and enable
  the [Mods Listing](https://steamcommunity.com/sharedfiles/filedetails/?id=588691634) mod; it will add the list of mods
  to the game log file.
* If you want an HTML file that lists mods, subscribe
  the [Stream It!](https://steamcommunity.com/sharedfiles/filedetails/?id=1597285962) mod (read workshop page for
  details of how to use it).

## Sharing your log file

Where are you contacting us?

### On Steam:

Log files are too big for Steam, so you'll have to upload the file somewhere. Here are some upload sites that people
commonly use:

* Drop file on to panel at [Uploadfiles.io](https://uploadfiles.io/) - free, no sign-up, can handle large files
* Paste contents in to [Paste.ee](https://paste.ee) or, if file is too big, use [ZeroBin](https://zerobin.net/) instead
* [Google Drive](https://drive.google.com/) ([how to upload?](https://support.google.com/drive/answer/2424368), [how to share?](https://support.google.com/drive/answer/2494822))
* [DropBox](https://www.dropbox.com) ([how to upload?](https://help.dropbox.com/files-folders/share/add-files), [how to share?](https://help.dropbox.com/files-folders/share/view-only-access))
* Do NOT use: ~~Pastebin~~ (too small size limit), ~~Dochub~~ (very slow to read files)

Make sure the file is publicly viewable, then share the URL in a comment.

### In Discord chat:

Drag the file in to the `#support` chat window to attach it. Also tell us why you're sharing the file, otherwise it's
just a random file and we have no idea what we're looking for.

### On GitHub:

On your issue ticket, drag and drop your log file in to the large text box. Wait for it to upload (the text will change
from `[Uploading ...]()` to something else), then click the green button (**Submit new issue**, if you're creating a new
issue, or **Comment**, if you're posting to existing issue).