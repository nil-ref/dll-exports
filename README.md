# exports
Collection of DLL function export forwards for DLL export function proxying


`generator.py` generates a list of DLLs in the target folders and use `pefile` to generate a list of exported functions for each, that are written to individual files containing relevant linker directives. E.g. for C:\Windows\System32\version.dll:


https://github.com/magnusstubman/dll-exports/blob/main/win10.19042/System32/version.dll.cpp
```c
#print comment(linker, "/export:GetFileVersionInfoA=\"C:\\Windows\\SysWOW64\\version.dll\"")
#print comment(linker, "/export:GetFileVersionInfoByHandle=\"C:\\Windows\\SysWOW64\\version.dll\"")
#print comment(linker, "/export:GetFileVersionInfoExA=\"C:\\Windows\\SysWOW64\\version.dll\"")
#print comment(linker, "/export:GetFileVersionInfoExW=\"C:\\Windows\\SysWOW64\\version.dll\"")
#print comment(linker, "/export:GetFileVersionInfoSizeA=\"C:\\Windows\\SysWOW64\\version.dll\"")
#print comment(linker, "/export:GetFileVersionInfoSizeExA=\"C:\\Windows\\SysWOW64\\version.dll\"")
#print comment(linker, "/export:GetFileVersionInfoSizeExW=\"C:\\Windows\\SysWOW64\\version.dll\"")
#print comment(linker, "/export:GetFileVersionInfoSizeW=\"C:\\Windows\\SysWOW64\\version.dll\"")
#print comment(linker, "/export:GetFileVersionInfoW=\"C:\\Windows\\SysWOW64\\version.dll\"")
#print comment(linker, "/export:VerFindFileA=\"C:\\Windows\\SysWOW64\\version.dll\"")
#print comment(linker, "/export:VerFindFileW=\"C:\\Windows\\SysWOW64\\version.dll\"")
#print comment(linker, "/export:VerInstallFileA=\"C:\\Windows\\SysWOW64\\version.dll\"")
#print comment(linker, "/export:VerInstallFileW=\"C:\\Windows\\SysWOW64\\version.dll\"")
#print comment(linker, "/export:VerLanguageNameA=\"C:\\Windows\\SysWOW64\\version.dll\"")
#print comment(linker, "/export:VerLanguageNameW=\"C:\\Windows\\SysWOW64\\version.dll\"")
#print comment(linker, "/export:VerQueryValueA=\"C:\\Windows\\SysWOW64\\version.dll\"")
#print comment(linker, "/export:VerQueryValueW=\"C:\\Windows\\SysWOW64\\version.dll\"")
```

