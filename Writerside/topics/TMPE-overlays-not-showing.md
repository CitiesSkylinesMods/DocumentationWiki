# TM:PE Overlays not Showing

> Article verified: August 2019

## Symptoms

* When selecting a tool on TM:PE menu bar, the overlays (vehicle restriction icons, lane arrows node selector circles,
  etc) are not appearing.
* You will probably see similar issues when trying to build roads or rails

## Cause

This is due to an issue with your graphics card not supporting shaders that the game requires.

You will likely see something like this in the game log file:

```
WARNING: Shader Unsupported: 'Hidden/Dof/DX11Dof' - Pass '' has no vertex shader
WARNING: Shader Unsupported: 'Hidden/Dof/DX11Dof' - Setting to default shader.
```

And you will probably see huge numbers of warnings in the log, like this:

```
d3d: failed to create 2D texture id=66947 w=1 h=1 mips=3 d3dfmt=21 [invalid call]
```

Most commonly this is due to **Intel graphics** - they are not complete graphics card; it's just a virtual graphics
device running on the CPU.

## Solution

There is no guaranteed solution, but there are a few things we can try...

* If the issue only affects road and rail building, see: [](Flickering-blue-road-building-guides.md)
* If interface text is missing (usually on Timed Traffic lights panel), see: [](Interface-text-missing.md)
* TM:PE 10.20.1 and earlier: If lane arrow buttons are missing, see: [](Lane-Arrows-buttons-missing-arrows.md)

If you're still having problems, you could try the following:

1. Make sure your graphics card drivers are fully updated.
2. If your computer has more than one graphics card (eg. integrated graphics and dedicated graphics):
    * Set the computer to use the dedicated graphics card
    * For more information, see **Hardware > Graphics**
      in [Performance Tuning Guide](https://steamcommunity.com/sharedfiles/filedetails/?id=465790009)
3. If you still have problems, try either (not both) the `-force-d3d9` (DirectX 9) or `-force-glcore` (
   OpenGL) [Launch Options](https://steamcommunity.com/sharedfiles/filedetails/?id=466981085)
    * If you have Intel UHD Graphics (Shader model 30 or above), however, don't use either of those launch options as it
      now supports the `Hidden/Dof/DX11Dof` DirectX 11 shaders. Note, however, that it's really, _really_, slow.

## Was it Fixed?

If not, and you are using an Intel graphics card, your only option is to upgrade to a dedicated graphics card.

Other issues? See: [](Troubleshooting.md)