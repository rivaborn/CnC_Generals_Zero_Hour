# Generals/Code/GameEngineDevice/Source/Win32Device/Common/Win32CDManager.cpp

## Purpose
Implements Windows-specific CD/DVD drive management for the game engine.

## Responsibilities
- Creates and manages Win32CDManager instances
- Detects CD/DVD drives on Windows systems
- Refreshes drive information and disk status
- Handles CD music file unloading when disks are removed

## Key Types
- Win32CDDrive (Class): Windows-specific CD drive implementation
- Win32CDManager (Class): Windows-specific CD manager implementation

## Key Functions
### CreateCDManager
- Purpose: Factory function to create a Win32CDManager instance
- Calls: NEW Win32CDManager

### Win32CDDrive::refreshInfo
- Purpose: Updates drive information and disk status
- Calls: GetVolumeInformation, TheFileSystem->unloadMusicFilesFromCD

### Win32CDManager::init
- Purpose: Initializes the CD manager and detects drives
- Calls: CDManager::init, destroyAllDrives, newDrive, refreshDrives, GetDriveType

### Win32CDManager::createDrive
- Purpose: Creates a new Win32CDDrive instance
- Calls: NEW Win32CDDrive

## Globals
None

## Dependencies
- windows.h
- Common/GameMemory.h
- Common/FileSystem.h
- Win32DEvice/Common/Win32CDManager.h
- CDManager (base class)
- CDDriveInterface (interface)
- CDManagerInterface (interface)
- TheFileSystem (global filesystem instance)
