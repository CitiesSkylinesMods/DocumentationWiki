> This is a work in progress

### Graphics quality

* Subscribe and enable Dynamic Resolution mod
* Set internal resolution to 250% (if your GPU can handle it; keep an eye on temperature!)
* Ideally do the recording during in-game golden hour (that hour where the sun is in just the right spot to make everything look super nice)

### Screen recording

* Use [bandicam](https://www.bandicam.com/downloads/) or similar screen recording app
* Set capture area to be 637x358 pixels (Steam specifies 636x358, but 63**7**x358 seems to work better)
* Clips should be no longer than 5-7 seconds

### Header and footer images

* These will be overlayed on top of the video
* Header: 637x50 pixels - should contain title and optionally an icon
* Footer: 637x30 pixels - should contain brief interaction guide (eg. info about which mouse button or keyboard shortcut to use)

> TODO: Style guide

### Conversion to GIF

Uploading:

* Upload the image to [Video to GIF](https://ezgif.com/video-to-gif)
* Size: Original (up to 800px)
* Frame rate: 5 (max 60 seconds)
* Method: FFMPEG
* Do _not_ select the 'Optimise for static background' checkbox

Add header:

* Use Overlay tool
* Upload header image
* Left: 0, Top: 0

Add footer:

* Use Overlay tool
* Upload footer image
* Left: 0, Top: 328 (or just drag the image to the bottom of the gif)

Optimise #1:

* Use Optimise tool
* Method: Remove duplicate frames
* Fuzz: ~30% (higher if it doesn't degrade quality)

Frames:

* Use Frames tool
* Set delay of first and last fames to 60
* Loop count: Leave blank (unlimited)

Optimise #2:

* Use Optimise tool
* Method: Optimise transparency
* Fuzz: ~15% (higher if it doesn't degrade quality)

Optimise #3:

* Use Optimise tool
* Method: Use single colour table for all frames

Save:

* You should now have a nice small GIF that can be uploaded to workshop page or wiki :)