# No Audio
> Article verified: October 2019

## Symptom

* No audio from Cities: Skylines

## Cause

This problem is _not_ caused by TM:PE. But seeing as you are here...

* [Nemo the fish app (Nahimic 2)](https://steamcommunity.com/app/255710/discussions/0/1649919326323114881/)
* Voicemeeter
* Sound settings in the game
* Mods
* Outdated drivers
* Various sound apps bundled with your computer or motherboard.

## Solutions

First check you don't have an app called `Nahimic 2` or `Voicemeeter` running; they break audio in some Unity games; uninstall them.

Next, check the following:

* Go in to game options and check sound settings
* Check your mods, particularly Ambient Sounds Tuner
* Note that while game is paused, audio stops

Other things:

* Make sure sound drivers are up-to-date: Go in to system information, find the sound drivers and you can update drivers in there.
* For Alienware machines, the problem is often the Alienware Sound Center app; open task manager and kill the sound center processes.
* Asus Sonic Studio 3 can cause problems; try disabling it.

FMOD errors:

* **Windows:** If you see an error like this in the log file:
> ```FMOD failed to get driver capabilities ... Error initializing output device.```
>  
> Go in to [Sound Settings](https://www.isunshare.com/windows-10/3-ways-to-open-sounds-settings-in-windows-10.html) and right-click then disable any sound devices you don't use (leave only one and the game will use that).
>  
> Or you might see this:
>  
> ```FMOD failed to initialize ... Error creating hardware sound buffer.```
>  
> That's caused by incompatible sample rate of your audio drivers. Try setting a different sample rate in Audio settings in Control Panel.
* **Mac / Linux:** If you see a more verbose error, like this:
> ``` FMOD failed to get number of drivers ...Error enumerating the available driver list.List may be inconsistent due to a recent device addition or removal Instantiation of FMOD effect type 3 failed UnityEditor.EditorAssemblies:SetLoadedEditorAssemblies(Assembly[])​```
>  
> Try disabling all unused sound devices as described above, and if that doesn't work, try installing Pulse Audio.

## Was it Fixed?

If not, consult the internet - this is clearly not a TM:PE problem.

Other issues? See: [](Troubleshooting.md)