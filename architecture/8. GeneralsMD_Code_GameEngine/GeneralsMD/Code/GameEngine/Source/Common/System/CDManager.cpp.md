# GeneralsMD/Code/GameEngine/Source/Common/System/CDManager.cpp

## Purpose
Manages CD drives and their associated disks in the game engine.

## Responsibilities
- Tracks CD drives and their paths
- Refreshes drive information periodically
- Provides access to drive count and individual drives
- Creates and destroys CD drive objects

## Key Types
- CDDrive (Class): Represents a single CD drive with path and disk info
- CDManager (Class): Manages collection of CD drives
- CDManagerInterface (Interface): Abstract interface for CD management

## Key Functions
### CDDrive::refreshInfo
- Purpose: Updates drive information (currently stub implementation)
- Calls: None

### CDManager::update
- Purpose: Periodically refreshes all drives (every 300 frames)
- Calls: refreshDrives()

### CDManager::newDrive
- Purpose: Creates and registers a new CD drive
- Calls: createDrive(), setPath()

### CDManager::refreshDrives
- Purpose: Updates information for all registered drives
- Calls: CDDrive::refreshInfo() for each drive

### CDManager::destroyAllDrives
- Purpose: Cleans up all registered drives
- Calls: None (directly deletes objects)

## Globals
- TheCDManager (CDManagerInterface*): Global instance of the CD manager

## Dependencies
- "Common/CDManager.h" (header)
- "GameLogic/GameLogic.h" (for frame counting)
- CD::Disk enum (from header)
- LListNode class (for drive storage)
- AsciiString class (for string handling)
