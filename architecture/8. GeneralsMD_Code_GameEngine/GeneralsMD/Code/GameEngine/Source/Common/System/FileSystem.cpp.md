# GeneralsMD/Code/GameEngine/Source/Common/System/FileSystem.cpp

## Purpose
Manages file system operations, including file access, directory listing, and CD-based music file handling.

## Responsibilities
- Provides singleton access to file system operations
- Delegates file operations to local and archive file systems
- Handles CD-based music file loading/unloading
- Caches file existence checks for performance

## Key Types
- FileSystem (Class): Main file system manager
- File (Class): File handle (defined elsewhere)
- FileInfo (Struct): File metadata (defined elsewhere)

## Key Functions
### FileSystem::openFile
- Purpose: Opens a file from local or archive file system
- Calls: TheLocalFileSystem->openFile, TheArchiveFileSystem->openFile

### FileSystem::doesFileExist
- Purpose: Checks if a file exists (with caching)
- Calls: TheNameKeyGenerator->nameToLowercaseKey, m_fileExist.find, TheLocalFileSystem->doesFileExist, TheArchiveFileSystem->doesFileExist

### FileSystem::areMusicFilesOnCD
- Purpose: Checks if music files are present on a CD drive
- Calls: TheCDManager->driveCount, TheCDManager->getDrive, TheLocalFileSystem->openFile

### FileSystem::loadMusicFilesFromCD
- Purpose: Loads music files from CD into archive system
- Calls: TheCDManager->driveCount, TheCDManager->getDrive, TheArchiveFileSystem->loadBigFilesFromDirectory

### FileSystem::unloadMusicFilesFromCD
- Purpose: Unloads music files from archive system
- Calls: TheAudio->isMusicPlayingFromCD, TheArchiveFileSystem->closeArchiveFile

## Globals
- TheFileSystem (FileSystem*): Singleton instance of the file system manager

## Dependencies
- Common/File.h, Common/FileSystem.h
- Common/ArchiveFileSystem.h, Common/LocalFileSystem.h
- Common/CDManager.h, Common/GameAudio.h
- Common/PerfTimer.h, Common/NameKeyGenerator.h (inferred)
