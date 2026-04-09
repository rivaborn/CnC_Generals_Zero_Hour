# GeneralsMD/Code/GameEngine/Source/Common/Audio/urllaunch.cpp

## Purpose
Handles URL launching functionality, including URL escaping and system integration via Windows shell commands.

## Responsibilities
- Escapes special characters in URLs
- Retrieves default browser command from Windows registry
- Launches URLs using the system's default browser

## Key Types
None

## Key Functions
### MakeEscapedURL
- Purpose: Escapes special characters in a URL and optionally prepends "file://"
- Calls: wcspbrk, wcslen, wcscpy, wcsncpy, swprintf

### GetShellOpenCommand
- Purpose: Retrieves the default browser command from Windows registry
- Calls: RegOpenKeyEx, RegQueryValueEx, RegCloseKey

### LaunchURL
- Purpose: Launches a URL using the system's default browser
- Calls: GetShellOpenCommand, CreateProcess, CloseHandle

## Globals
None

## Dependencies
- Common/URLLaunch.h
- Windows API: RegOpenKeyEx, RegQueryValueEx, RegCloseKey, CreateProcess, CloseHandle
- C runtime: wcspbrk, wcslen, wcscpy, wcsncpy, swprintf, wsprintf, _tcsstr, _tcschr, _tcslen, _tcsncpy
