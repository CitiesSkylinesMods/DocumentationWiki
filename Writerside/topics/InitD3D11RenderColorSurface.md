# InitD3D11RenderColorSurface VRDevice Error
## Symptom

The game will freeze (although mouse and music might still work) during or after loading a save, and you'll see an error in the game log file similar to:

* `InitD3D11RenderColorSurface: VRDevice said it created a texture, but the texture is NULL. VR platform drivers may be running with elevated privileges.`

## Cause

The graphics driver is running in VR mode, but the game doesn't support VR.

## Solution

Exit to desktop (Alt+F4 will usually work if the screen has frozen).

Make sure your graphics card drivers are fuly up-to-date. Manually check the manufacturer website for updates if necessary.

If you have NVIDIA graphics card, download GeForce Experience app and scan for games. Once it's found the game, it should prevent the issue from happening in future.

Check your Steam global settings and also game settings and disable anything that looks VR related.

## Was it Fixed?

If not, try adding the `-force-d3d9` [launch option](https://steamcommunity.com/sharedfiles/filedetails/?id=466981085) as a last resort.

Other issues? See: [](Troubleshooting.md)