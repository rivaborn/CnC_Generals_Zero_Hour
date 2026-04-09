# Generals/Code/GameEngine/Source/Common/System/FileSystem.cpp

## Purpose
This file implements the `FileSystem` class, which manages file operations in the game engine. It provides a unified interface for accessing files from both local storage and archive files.

## Responsibilities
- Manages initialization and update of file systems.
- Provides methods to open files, check if files exist, list directory contents, and get file information.
- Handles music file loading and unloading from CDs.

## Key Types
- `FileSystem` (Class): Singleton class for managing file operations.
- `File` (Class): Represents an open file.
- `ArchiveFileSystem` (Class): Manages archive files.
- `LocalFileSystem` (Class): Manages local file system access.
- `CDManager` (Class): Manages CD drives.

## Key Functions
### FileSystem::init
- Purpose: Initializes the local and archive file systems.
- Calls: 
  - `TheLocalFileSystem->init()`
  - `TheArchiveFileSystem->init()`

### FileSystem::update
- Purpose: Updates the local and archive file systems.
- Calls:
  - `TheLocalFileSystem->update()`
  - `TheArchiveFileSystem->update()`

### FileSystem::openFile
- Purpose: Opens a file, first trying the local file system and then the archive file system if not found locally.
- Calls:
  - `TheLocalFileSystem->openFile()`
  - `TheArchiveFileSystem->openFile()`

### FileSystem::doesFileExist
- Purpose: Checks if a file exists in either the local or archive file systems.
- Calls:
  - `TheLocalFileSystem->doesFileExist()`
  - `TheArchiveFileSystem->doesFileExist()`

### FileSystem::getFileListInDirectory
- Purpose: Retrieves a list of files in a directory from both the local and archive file systems.
- Calls:
  - `TheLocalFileSystem->getFileListInDirectory()`
  - `TheArchiveFileSystem->getFileListInDirectory()`

### FileSystem::getFileInfo
- Purpose: Gets information about a file, checking both the local and archive file systems.
- Calls:
  - `TheLocalFileSystem->getFileInfo()`
  - `TheArchiveFileSystem->getFileInfo()`

### FileSystem::createDirectory
- Purpose: Creates a directory in the local file system.
- Calls:
  - `TheLocalFileSystem->createDirectory()`

### FileSystem::areMusicFilesOnCD
- Purpose: Checks if music files are available on any connected CD drives.
- Calls:
  - `TheCDManager->driveCount()`
  - `TheCDManager->getDrive()`
  - `TheLocalFileSystem->openFile()`

### FileSystem::loadMusicFilesFromCD
- Purpose: Loads music files from a CD drive into the archive file system.
- Calls:
  - `TheArchiveFileSystem->loadBigFilesFromDirectory()`

### FileSystem::
