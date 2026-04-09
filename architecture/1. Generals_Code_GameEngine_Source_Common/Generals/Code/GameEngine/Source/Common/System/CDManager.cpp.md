# Generals/Code/GameEngine/Source/Common/System/CDManager.cpp

## Purpose
This file implements the CDManager and CDDrive classes, responsible for managing CD drives and their contents in the game.

## Responsibilities
- Manages CD drives and their information.
- Checks if CDs are still in the drive periodically.
- Provides methods to get drive paths, disk names, and disk IDs.

## Key Types
- **CDDrive (Class)**: Represents a CD drive with properties like path, disk name, and disk ID.
- **CDManager (Class)**: Manages multiple CDDrive instances, providing methods to initialize, update, and reset the drives.

## Key Functions
### CDDrive::refreshInfo
- Purpose: Refreshes the information about the CD in the drive.
- Calls: None

### CDManager::update
- Purpose: Updates the CD manager every frame, checking if CDs are still in the drive.
- Calls: refreshDrives

### CDManager::newDrive
- Purpose: Creates a new CDDrive instance and adds it to the list of managed drives.
- Calls: createDrive

### CDManager::refreshDrives
- Purpose: Refreshes information for all managed CD drives.
- Calls: None

### CDManager::destroyAllDrives
- Purpose: Destroys all managed CDDrive instances.
- Calls: None

## Globals
- **TheCDManager (CDManagerInterface*)**: Global instance of the CD manager.

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/CDManager.h"
  - "GameLogic/GameLogic.h"
