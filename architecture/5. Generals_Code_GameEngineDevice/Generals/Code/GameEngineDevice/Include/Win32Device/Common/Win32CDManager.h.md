# Generals/Code/GameEngineDevice/Include/Win32Device/Common/Win32CDManager.h

## Purpose
Declares Win32-specific CD drive management classes for the SAGE engine.

## Responsibilities
- Defines Win32CDDrive and Win32CDManager classes
- Provides CD drive detection and refresh functionality
- Implements platform-specific CD management interface

## Key Types
- **Win32CDDrive (Class)**: Win32 implementation of CD drive interface
- **Win32CDManager (Class)**: Win32 CD manager that handles drive detection and updates

## Key Functions
### Win32CDDrive::refreshInfo
- Purpose: Update drive information
- Calls: Not inferable

### Win32CDManager::init
- Purpose: Initialize CD manager
- Calls: Not inferable

### Win32CDManager::update
- Purpose: Update CD manager state
- Calls: Not inferable

### Win32CDManager::reset
- Purpose: Reset CD manager
- Calls: Not inferable

### Win32CDManager::refreshDrives
- Purpose: Refresh all CD drive information
- Calls: Not inferable

### Win32CDManager::createDrive
- Purpose: Factory method to create CD drive instances
- Calls: Not inferable

## Globals
- None

## Dependencies
- **CDManager.h**: Base class interface
- **CDDrive**: Base CD drive interface (inherited by Win32CDDrive)
