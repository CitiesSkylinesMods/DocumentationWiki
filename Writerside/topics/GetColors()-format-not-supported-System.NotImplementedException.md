# GetColors() format not supported System.NotImplementedException

> Article verified: June 2019

## Symptom

You see an error message similar to the following (either on-screen or in the log file):

* `GetColors(): format not supported [System.NotImplementedException]`

## Cause

This error is not caused by TM:PE.

It's caused by putting invalid file in to one of the game folders. The full error shown in the log file will give some
idea of where the file might be, for example this one is in the `brushes` folder:

```
System.NotImplementedException GetColors(): format not supported
at System.Environment.get_StackTrace()
at BrushOptionPanel.Refresh()
at BrushOptionPanel.Start()
```

A common cause is putting height maps in to the brushes folder by mistake.

## Solution

> Thanks to Double Drick for this solution!

Check your game folders for any images or other files that shouldn't be there and remove them.

## Was it Fixed?

If not, check the internet - there may be similar issues with unrecognized files in other folders.

Something else? See: [](Troubleshooting.md)