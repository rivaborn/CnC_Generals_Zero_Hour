# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/W3DFileSystem.cpp

## Purpose
Implements a file system abstraction for W3D (3D model) and image files (TGA/DDS) in the SAGE engine, handling file lookup across multiple directories including localization paths and user data.

## Responsibilities
- Manages file paths for W3D, TGA, and DDS files
- Handles file existence checks across multiple directories
- Provides file I/O operations (open/read/seek/close)
- Supports localization and user-modifiable assets
- Overrides default W3D file factory

## Key Types
- `GameFileType` (Enum): File type identifiers (W3D/TGA/DDS/unknown)
- `GameFileClass` (Class): File handle wrapper with path resolution
- `W3DFileSystem` (Class): File factory singleton for W3D assets

## Key Functions
### `Set_Name`
- Purpose: Resolves file path across multiple directories based on file type
- Calls: `TheFileSystem->doesFileExist`, `isImageFileType`

### `Open`
- Purpose: Opens a file for reading using resolved path
- Calls: `TheFileSystem->openFile`

### `isImageFileType`
- Purpose: Checks if file type is TGA or DDS
- Calls: None

## Globals
- `TheW3DFileSystem` (W3DFileSystem*): Singleton instance of W3D file system

## Dependencies
- `Common/File.h`, `Common/FileSystem.h`, `Common/GlobalData.h`
- `W3DDevice/GameClient/W3DFileSystem.h`
- `TheFileSystem`, `TheGlobalData` (external globals)
