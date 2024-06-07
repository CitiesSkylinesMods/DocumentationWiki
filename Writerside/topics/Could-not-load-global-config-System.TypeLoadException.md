## Symptom

An error in the `TMPE.log` file stating:

```
Could not load global config: System.TypeLoadException: Could not load type 'System.Xml.Serialization.XmlRootAttribute' from assembly 'System.Xml, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089'.
  at TrafficManager.State.GlobalConfig.Load (System.DateTime& modifiedTime) [0x00000] in <filename unknown>:0  Generating default config.
   at CSUtil.Commons.Log.LogToFile(System.String log, LogLevel level)
```

This issue only seems to affect Windows users.

## Cause

This is caused by insufficient permissions on the folder that contain the TM:PE [Global Configuration](Global Configuration) file.

## Solution

1. Locate the `TMPE_GlobalConfig.xml` file on disk.
   * Usually `C:\Program Files (x86)\Steam\steamapps\common\Cities_Skylines`
2. Either give the folder more permissions for your user, or run the game as Administrator

(We are investigating better locations for the config file, but for now that is the only fix).

## Fixed?

If not, please let us know: [Report a bug](Report a bug)

Other issues? See: [Troubleshooting](Troubleshooting)