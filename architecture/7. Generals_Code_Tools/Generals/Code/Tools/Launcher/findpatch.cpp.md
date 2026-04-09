# Generals/Code/Tools/Launcher/findpatch.cpp

## Purpose
Handles patch file detection and cleanup for the game launcher.

## Responsibilities
- Locates patch files in game directories
- Retrieves application installation paths from registry
- Deletes patch files after application

## Key Types
- None

## Key Functions
### Find_Patch
- Purpose: Searches for patch files in game directories
- Calls: Get_App_Dir, FindFirstFile, FindClose

### Get_App_Dir
- Purpose: Retrieves installation path for a specific SKU from registry
- Calls: RegOpenKeyEx, RegQueryValueEx

### Delete_Patches
- Purpose: Removes patch files from all game directories
- Calls: Get_App_Dir, FindFirstFile, FindNextFile, FindClose

## Globals
- None

## Dependencies
- findpatch.h
- ConfigFile class
- Windows API (FindFirstFile, RegOpenKeyEx, etc.)
- Wstring class
