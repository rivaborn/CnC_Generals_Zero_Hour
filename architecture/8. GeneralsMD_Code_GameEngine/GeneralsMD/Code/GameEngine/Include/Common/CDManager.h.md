# GeneralsMD/Code/GameEngine/Include/Common/CDManager.h

## Purpose
Defines interfaces and classes for managing CD-ROM drives and detecting game disks.

## Responsibilities
- Provides abstract interfaces for CD drive and manager functionality
- Implements concrete CD drive and manager classes
- Manages a list of detected CD drives
- Supports disk detection and path management

## Key Types
- Disk (Enum): Disk identifiers (UNKNOWN_DISK, NO_DISK, ANY_DISK, DISK_1, NUM_DISKS)
- CDDriveInterface (Class): Abstract interface for CD drive operations
- CDDrive (Class): Concrete implementation of CD drive functionality
- CDManagerInterface (Class): Abstract interface for CD manager operations
- CDManager (Class): Concrete implementation of CD manager functionality

## Key Functions
### CreateCDManager
- Purpose: Factory function to create CDManager instance
- Calls: Not inferable

## Globals
- TheCDManager (CDManagerInterface*): Global pointer to the CD manager instance

## Dependencies
- Common/List.h
- Common/SubSystemInterface.h
- Common/AsciiString.h
