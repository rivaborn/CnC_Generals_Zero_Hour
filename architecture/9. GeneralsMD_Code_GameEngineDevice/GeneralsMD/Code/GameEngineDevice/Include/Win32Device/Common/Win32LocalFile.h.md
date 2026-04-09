# GeneralsMD/Code/GameEngineDevice/Include/Win32Device/Common/Win32LocalFile.h

## Purpose
Declares the Win32LocalFile class, a platform-specific implementation of LocalFile for Windows.

## Responsibilities
- Provides Win32-specific file operations
- Inherits from LocalFile base class
- Manages memory allocation via MEMORY_POOL_GLUE

## Key Types
- Win32LocalFile (Class): Win32 implementation of LocalFile
- Win32LocalFileMagicEnum (Enum): Not inferable
- Win32LocalFile_GLUE_NOT_IMPLEMENTED (Enum): Not inferable

## Key Functions
### Win32LocalFile()
- Purpose: Constructor for Win32LocalFile
- Calls: None

## Globals
- None

## Dependencies
- Common/LocalFile.h
- MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE macro
