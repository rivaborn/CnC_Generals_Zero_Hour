# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DFileSystem.h

## Purpose
Defines the W3D file system abstraction for loading game assets via GDI file interface.

## Responsibilities
- Provides `GameFileClass` for file operations (open, read, seek, etc.)
- Implements `W3DFileSystem` as a file factory using GDI assets
- Manages file instance pooling via `Get_File`/`Return_File`
- Handles both legacy GDI assets and flat directory access

## Key Types
- **GameFileClass (Class)**: Wraps file I/O operations with GDI asset support
- **W3DFileSystem (Class)**: File factory that uses GDI assets for W3D/targa files
- **FileClass (External)**: Base class for file operations (inherited)

## Key Functions
### GameFileClass::Is_Available
- Purpose: Checks if the file exists and is accessible
- Calls: Not inferable (implementation in .cpp)

### W3DFileSystem::Get_File
- Purpose: Retrieves a file instance by name
- Calls: Not inferable

### W3DFileSystem::Return_File
- Purpose: Returns a file instance to the pool
- Calls: Not inferable

## Globals
- **TheW3DFileSystem (W3DFileSystem*)**: Global instance of the W3D file system

## Dependencies
- `WWLIB/ffactory.h` (FileFactoryClass)
- `Common/File.h` (FileClass)
- `File` (external class for actual file operations)
