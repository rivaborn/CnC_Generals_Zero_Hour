# Generals/Code/Libraries/Source/WWVegas/WWLib/LaunchWeb.cpp

## Purpose
Launches the default web browser to display a specified URL.

## Responsibilities
- Creates a temporary HTML file to determine the default browser executable
- Launches the browser with the given URL
- Handles cleanup of temporary files
- Validates inputs and process creation

## Key Types
None

## Key Functions
### LaunchWebBrowser
- Purpose: Launches the default web browser to view the specified URL
- Calls: `strlen`, `GetWindowsDirectory`, `GetTempFileName`, `strrchr`, `strcpy`, `CreateFile`, `WriteFile`, `CloseHandle`, `FindExecutable`, `DeleteFile`, `sprintf`, `memset`, `CreateProcess`

## Globals
None

## Dependencies
- `LaunchWeb.h`
- `<windows.h>`
- `<shellapi.h>`
- `<stdio.h>`
- `<assert.h>`
