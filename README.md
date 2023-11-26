# Clang(d?) bug repro

Please run with:

```sh
cmake -Bbuild -DCMAKE_EXPORT_COMPILE_COMMANDS=ON -G "Unix Makefiles"
cmake --build build
```

`build/compile_commands.json` should look like the following if you cannot run the above commands for some reason:

```json
[
{
  "directory": "<your_dir>/clang_bug_repro/build/BadApp",
  "command": "/Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin/cc  -I<your_dir>/clang_bug_repro/BadModule -x objective-c -std=gnu17 -arch arm64 -isysroot /Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.0.sdk -fmodules -o CMakeFiles/BadApp.dir/main.m.o -c <your_dir>/clang_bug_repro/BadApp/main.m",
  "file": "<your_dir>/clang_bug_repro/BadApp/main.m",
  "output": "BadApp/CMakeFiles/BadApp.dir/main.m.o"
}
]
```
