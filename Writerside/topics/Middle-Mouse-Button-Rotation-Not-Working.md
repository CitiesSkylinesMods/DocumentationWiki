# Middle Mouse Camera Rotation Not Working

> Verified: April 2022 - TM:PE 11.6.5.2

## Symptom

* Middle mouse button not rotating the camera

## Cause

This bug is _not_ caused by TM:PE.

* Faulty mouse button
* Stuck keyboard modifier key (eg. `Alt`, `Shift` or `Ctrl`)

## Solution

First, try `Alt`+`Tab` to switch to another application, then `Alt`+`Tab` to return to the game - this sometimes fixes
it.

If that doesn't work:

1. In game (from main menu or the pause menu) go to **Options** screen
2. Select **Keybindings** then select **Shared**
3. Find the rotate map shortcut that is currently assigned to **Middle Mouse Button**
4. Click that shortcut to edit it, then press `Middle Mouse Button`

If pressing the `Middle Mouse Button` doesn't change the shortcut, then it is likely a problem with your mouse. Try a
different mouse and see if that solves the issue.

If the shortcut changes to something like **Alt + Middle Mouse Button** (or some other modifier key) then you've got a
sticky key on your keyboard. Pressing the key a few times might un-stick it, in which case you'll need to set the
shortcut again (it will now just show **Middle Mouse Button**).

## Was it Fixed?

If not, consult the internets :/

Other issues? See: [](Troubleshooting.md)