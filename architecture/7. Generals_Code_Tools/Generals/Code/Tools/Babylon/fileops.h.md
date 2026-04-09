# Generals/Code/Tools/Babylon/fileops.h

## Purpose
Header file defining file I/O utility functions and file attribute flags.

## Responsibilities
- Declares file existence and attribute checking functions
- Defines file attribute bit flags
- Declares backup/restore file operations

## Key Types
- None

## Key Functions
### FileExists
- Purpose: Check if a file exists
- Calls: Not inferable

### FileAttribs
- Purpose: Get file attributes
- Calls: Not inferable

### MakeBackupFile
- Purpose: Create a backup of a file
- Calls: Not inferable

### RestoreBackupFile
- Purpose: Restore a file from backup
- Calls: Not inferable

## Globals
- FA_NOFILE (int): Flag indicating no file exists
- FA_READONLY (int): Flag indicating file is read-only
- FA_DIRECTORY (int): Flag indicating path is a directory
- FA_WRITEABLE (int): Flag indicating file is writable

## Dependencies
- None visible in header
