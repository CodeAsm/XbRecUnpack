# XbRecUnpack, ported to Linux

Tool for extracting Xbox/Xbox360 SDKs & recoveries.
Using Linux as your host in this case. and ported to .NET 10

```
Usage:
  XbRecUnpack [-L/-R] <path-to-recctrl.bin> [output-folder]
  XbRecUnpack [-L/-R] <path-to-SDK/remote-recovery.exe> [output-folder]
  XbRecUnpack [-L/-R] <path-to-recovery.iso> [output-folder]
  XbRecUnpack [-L/-R] <path-to-recovery.zip> [output-folder]
Will try extracting all files to the given output folder
If output folder isn't specified, will extract to "<input-file-path>_ext"
-L will only list entries inside input file without extracting them
-R will print info about any extracted X360 xboxrom images
  (if -R isn't used, will print a summary instead)
```
