# Generals/Code/Tools/wolSetup/verchk.cpp

## Purpose
This file provides version information retrieval utilities for the WOL setup tool.

## Responsibilities
- Retrieve version information from executable files
- Check if WOL API is installed by examining version info
- Manage memory allocation for version info buffers

## Key Types
- None

## Key Functions
### GetVersionInfo
- Purpose: Retrieves version information from a file's version resource
- Calls: `GetFileVersionInfoSize`, `GlobalAlloc`, `GlobalLock`, `GetFileVersionInfo`, `VerQueryValue`, `memcpy`, `GlobalUnlock`, `GlobalFree`

### loadWolapi
- Purpose: Checks if WOL API is installed by examining version info
- Calls: `GetVersionInfo`

## Globals
- `g_wolapiInstalled` (bool): Tracks whether WOL API is installed

## Dependencies
- `verchk.h`, `wolsetup.h`
- Windows API: `GetFileVersionInfoSize`, `GetFileVersionInfo`, `VerQueryValue`, `GlobalAlloc`, `GlobalLock`, `GlobalUnlock`, `GlobalFree`
- C runtime: `memcpy`
