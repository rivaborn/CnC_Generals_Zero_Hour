# GeneralsMD/Code/GameEngineDevice/Include/Win32Device/Common/Win32CDManager.h

## Purpose
Declares Win32-specific CD drive management classes for the SAGE engine.

## Responsibilities
- Defines Win32CDDrive and Win32CDManager classes
- Provides platform-specific CD drive interface implementations
- Manages CD drive initialization, updates, and refresh operations

## Key Types
- **Win32CDDrive (Class)**: Win32 implementation of CDDrive interface
- **Win32CDManager (Class)**: Win32 implementation of CDManager interface

## Key Functions
### Win32CDDrive::refreshInfo
- Purpose: Update drive information
- Calls: Not inferable

### Win32CDManager::init
- Purpose: Initialize CD manager subsystem
- Calls: Not inferable

### Win32CDManager::update
- Purpose: Update CD manager state
- Calls: Not inferable

### Win32CDManager::reset
- Purpose: Reset CD manager subsystem
- Calls: Not inferable

### Win32CDManager::refreshDrives
- Purpose: Refresh information for all CD drives
- Calls: Not inferable

### Win32CDManager::createDrive
- Purpose: Factory method to create new CD drive instances
- Calls: Not inferable

## Globals
- None

## Dependencies
- **CDManager.h**: Base class interface definitions
- **CDDrive**: Base class for CD drive functionality
