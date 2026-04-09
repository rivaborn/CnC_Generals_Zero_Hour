# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/LaunchWeb.cpp

## Purpose
Launches the default web browser to display a specified URL.

## Responsibilities
- Creates a temporary HTML file to determine the default browser executable
- Uses Windows API to find and launch the appropriate browser
- Handles URL validation and process creation

## Key Types
- None

## Key Functions
### LaunchWebBrowser
- Purpose: Launches the default web browser with the specified URL
- Calls: `strlen`, `GetWindowsDirectory`, `GetTempFileName`, `strrchr`, `strcpy`, `CreateFile`, `WriteFile`, `CloseHandle`, `FindExecutable`, `DeleteFile`, `sprintf`, `memset`, `CreateProcess`

## Globals
- None

## Dependencies
- `LaunchWeb.h`
- Windows API headers: `<windows.h>`, `<shellapi.h>`
- Standard C headers: `<stdio.h>`, `<assert.h>`
