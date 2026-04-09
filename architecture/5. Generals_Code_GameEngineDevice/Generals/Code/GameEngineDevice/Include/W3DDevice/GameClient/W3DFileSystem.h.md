# Generals/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DFileSystem.h

## Purpose
Defines the W3D file system interface for loading game assets using GDI file operations.

## Responsibilities
- Provides file access abstraction for W3D assets
- Manages file factory pattern for asset loading
- Handles both legacy GDI assets and current flat directory assets
- Tracks file availability and state

## Key Types
- **GameFileClass (Class)**: File access wrapper for game assets
- **W3DFileSystem (Class)**: File factory implementation using GDI assets
- **FileFactoryClass (External)**: Base class for file factory pattern

## Key Functions
### GameFileClass::Open
- Purpose: Opens a file with specified access rights
- Calls: Not inferable

### W3DFileSystem::Get_File
- Purpose: Retrieves a file instance from the file system
- Calls: Not inferable

### W3DFileSystem::Return_File
- Purpose: Returns a file instance to the file system
- Calls: Not inferable

## Globals
- **TheW3DFileSystem (W3DFileSystem*)**: Global instance of the W3D file system

## Dependencies
- `WWLIB/ffactory.h` (FileFactoryClass)
- `Common/File.h` (FileClass)
- Standard C++ file I/O headers
