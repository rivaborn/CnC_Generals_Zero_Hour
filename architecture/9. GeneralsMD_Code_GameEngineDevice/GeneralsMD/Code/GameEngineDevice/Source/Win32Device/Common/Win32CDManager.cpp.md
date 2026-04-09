# GeneralsMD/Code/GameEngineDevice/Source/Win32Device/Common/Win32CDManager.cpp

## Purpose
Implements Windows-specific CD/DVD drive management for the game engine.

## Responsibilities
- Creates and manages Win32CDManager instance
- Detects CD/DVD drives on Windows systems
- Refreshes drive information and disk status
- Handles CD music file unloading when disks are removed

## Key Types
- Win32CDDrive (Class): Windows-specific CD drive implementation
- Win32CDManager (Class): Windows-specific CD manager implementation

## Key Functions
### CreateCDManager
- Purpose: Factory function to create Win32CDManager instance
- Calls: None

### Win32CDDrive::refreshInfo
- Purpose: Updates drive information and disk status
- Calls: GetVolumeInformation, TheFileSystem->unloadMusicFilesFromCD

### Win32CDManager::init
- Purpose: Initializes CD manager and detects drives
- Calls: CDManager::init, destroyAllDrives, newDrive, refreshDrives, GetDriveType

### Win32CDManager::createDrive
- Purpose: Creates new Win32CDDrive instance
- Calls: None

## Globals
None

## Dependencies
- windows.h
- Common/GameMemory.h
- Common/FileSystem.h
- Win32DEvice/Common/Win32CDManager.h
- CDManager (base class)
- CDDriveInterface (interface)
- CD (enum)
- TheFileSystem (global)
