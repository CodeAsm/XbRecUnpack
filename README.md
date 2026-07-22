# XbRecUnpack, ported to Linux

Tool for extracting Xbox/Xbox360 SDKs & recoveries.
Using Linux as your host in this case. and ported to .NET 10

**Original windows version: https://github.com/emoose/XbRecUnpack**

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

example:
```sh
./XbRecUnpack/bin/Release/net10.0/linux-x64/XbRecUnpack -R ../../0530_Xenon_Recovery/recctrl.bin out/
```

## Building under Linux

install the dotnet SDK, on Arch this can be done with:
```powershell
sudo pacman -S dotnet-sdk
```

clone:
```sh
git clone https://github.com/CodeAsm/XbRecUnpack
cd XbRecUnpack/
```
now build it:

```sh
dotnet publish -c Release -r linux-x64 --self-contained true
```
