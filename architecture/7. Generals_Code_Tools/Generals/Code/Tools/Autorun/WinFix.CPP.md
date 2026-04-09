# Generals/Code/Tools/Autorun/WinFix.CPP

## Purpose
This file provides Windows version detection functionality for the game's setup/autorun tools.

## Responsibilities
- Detects the Windows OS version and build information
- Provides version string formatting
- Logs version data to a debug file
- Checks minimum version requirements

## Key Types
- **WindowsVersionInfo (Class)**: Tracks OS version, build, and platform details
- **OSVERSIONINFO (Struct)**: Windows API struct for version data (external)

## Key Functions
### WindowsVersionInfo::WindowsVersionInfo
- Purpose: Initializes version detection and logs results
- Calls: `GetVersionEx`, `Msg`, `RegOpenKeyEx`, `RegQueryValueEx`, `RegCloseKey`

### WindowsVersionInfo::Version_String
- Purpose: Returns human-readable OS version string
- Calls: `strcpy`, `strcat`

### WindowsVersionInfo::Version_Name
- Purpose: Returns formatted version name string
- Calls: None

### WindowsVersionInfo::Meets_Minimum_Version_Requirements
- Purpose: Checks if OS meets minimum requirements (Windows 4.0+)
- Calls: None

## Globals
- **WinVersion (WindowsVersionInfo)**: Global instance for version detection

## Dependencies
- `<windows.h>`, `<windowsx.h>`, `<stdio.h>`, `<assert.h>`
- `winfix.h`, `wnd_file.h`
- Windows API: `GetVersionEx`, registry functions
- Internal: `Msg`, `Delete_Msg_File`
