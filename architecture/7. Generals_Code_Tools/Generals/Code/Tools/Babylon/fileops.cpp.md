# Generals/Code/Tools/Babylon/fileops.cpp

## Purpose
Provides file system operations for checking file existence, attributes, and backup/restore functionality.

## Responsibilities
- Check file existence and attributes
- Generate backup file names
- Create and restore file backups

## Key Types
- None

## Key Functions
### FileExists
- Purpose: Check if a file exists and is not a directory.
- Calls: FileAttribs

### FileAttribs
- Purpose: Get file attributes (directory, read-only, writable).
- Calls: FindFirstFile, FindClose

### make_bk_name
- Purpose: Generate a backup file name by appending "_back_up" before the extension.
- Calls: strcpy, strchr, strcat

### MakeBackupFile
- Purpose: Create a backup copy of a file.
- Calls: make_bk_name, CopyFile

### RestoreBackupFile
- Purpose: Restore a file from its backup if it exists.
- Calls: make_bk_name, FileExists, CopyFile

## Globals
- None

## Dependencies
- stdAfx.h, fileops.h
- Windows API: FindFirstFile, FindClose, CopyFile
- C runtime: strcpy, strchr, strcat
