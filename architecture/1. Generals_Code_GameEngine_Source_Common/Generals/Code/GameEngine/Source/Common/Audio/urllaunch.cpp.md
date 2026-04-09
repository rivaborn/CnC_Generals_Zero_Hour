# Generals/Code/GameEngine/Source/Common/Audio/urllaunch.cpp

## Purpose
This file contains functions for handling URL launching, including escaping URLs and determining the appropriate shell command to open them.

## Responsibilities
- Escaping special characters in URLs.
- Retrieving the shell command associated with a given protocol or file extension.
- Launching URLs using the retrieved shell command.

## Key Types
- None

## Key Functions
### MakeEscapedURL
- Purpose: Escapes special characters in a URL to ensure it is properly formatted.
- Calls: `wcsstr`, `wcspbrk`, `new`, `wcscpy`, `wcsncpy`, `swprintf`

### GetShellOpenCommand
- Purpose: Retrieves the shell command associated with opening URLs, either through file extension or protocol.
- Calls: `RegOpenKeyEx`, `RegQueryValueEx`, `_tcsstr`, `_tcschr`, `_tcsncpy`

### LaunchURL
- Purpose: Constructs and executes a command to launch a URL using the appropriate application.
- Calls: `GetShellOpenCommand`, `wsprintf`, `CreateProcess`, `CloseHandle`

## Globals
- None

## Dependencies
- Key includes:
  - `"Common/URLLaunch.h"`
- External symbols used but not defined here:
  - Windows API functions like `RegOpenKeyEx`, `RegQueryValueEx`, `CreateProcess`, `CloseHandle`
  - Standard C++ library functions like `wcsstr`, `wcspbrk`, `new`, `wcscpy`, `wcsncpy`, `swprintf`
