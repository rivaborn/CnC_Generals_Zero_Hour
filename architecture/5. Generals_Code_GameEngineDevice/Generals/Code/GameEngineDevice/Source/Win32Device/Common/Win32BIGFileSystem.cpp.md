# Generals/Code/GameEngineDevice/Source/Win32Device/Common/Win32BIGFileSystem.cpp

## Purpose
Implements the Win32-specific BIG file system for loading and managing archive files in the game.

## Responsibilities
- Loads and parses BIG archive files from the filesystem
- Manages a map of open archive files
- Provides methods to open/close archive files and load them into the directory tree
- Handles special cases for music BIG files (audio cleanup)

## Key Types
- Win32BIGFileSystem (Class): Manages BIG archive files on Win32
- BIGFileIdentifier (const char*): String identifier for BIG files ("BIGF")

## Key Functions
### Win32BIGFileSystem::init
- Purpose: Initializes the BIG file system and loads BIG files from the directory
- Calls: TheLocalFileSystem->openFile, loadBigFilesFromDirectory

### Win32BIGFileSystem::openArchiveFile
- Purpose: Opens and parses a BIG archive file, extracting file entries
- Calls: TheLocalFileSystem->openFile, NEW Win32BIGFile, fp->read, fp->seek, archiveFile->addFile, archiveFile->attachFile

### Win32BIGFileSystem::closeArchiveFile
- Purpose: Closes a specific BIG archive file and cleans up resources
- Calls: TheAudio->stopAudio (for music BIG), delete

### Win32BIGFileSystem::loadBigFilesFromDirectory
- Purpose: Loads all BIG files matching a mask from a directory
- Calls: TheLocalFileSystem->getFileListInDirectory, openArchiveFile, loadIntoDirectoryTree

## Globals
- BIGFileIdentifier (const char*): String identifier for BIG files ("BIGF")

## Dependencies
- ArchiveFileSystem, Win32BIGFile, LocalFileSystem, File, AudioAffect, GameAudio
- Winsock2.h for network byte order functions (ntohl)
