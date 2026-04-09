# Generals/Code/GameEngineDevice/Source/W3DDevice/GameClient/W3DFileSystem.cpp

## Purpose
Implements a file system abstraction for W3D (W3D Device) that handles file access for W3D models, TGA, and DDS textures, with support for legacy and test assets.

## Responsibilities
- Manages file paths for different asset types (W3D, TGA, DDS)
- Provides file I/O operations (open, read, seek, close)
- Supports multiple asset directories (main, legacy, test, user, localized)
- Determines file availability and type
- Overrides default W3D file factory

## Key Types
- GameFileType (Enum): file type identifiers (W3D, TGA, DDS, UNKNOWN)
- GameFileClass (Class): wraps file operations with path resolution
- W3DFileSystem (Class): file factory that overrides default W3D file handling

## Key Functions
### isImageFileType
- Purpose: checks if a file type is an image format (TGA or DDS)
- Calls: None

### GameFileClass::Set_Name
- Purpose: sets filename and resolves full path based on file type
- Calls: TheFileSystem->doesFileExist, TheGlobalData->getPath_UserData, GetRegistryLanguage

### W3DFileSystem::Get_File
- Purpose: creates a new GameFileClass instance for a given filename
- Calls: NEW operator

### W3DFileSystem::Return_File
- Purpose: deletes a previously obtained file
- Calls: delete operator

## Globals
- TheW3DFileSystem (W3DFileSystem*): global instance of the W3D file system

## Dependencies
- Common/Debug.h, Common/File.h, Common/FileSystem.h, Common/GlobalData.h, Common/MapObject.h, Common/Registry.h, W3DDevice/GameClient/W3DFileSystem.h
- TheFileSystem, TheGlobalData, _TheFileFactory (external symbols)
