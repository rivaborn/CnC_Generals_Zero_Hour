# Generals/Code/Tools/Autorun/Wnd_file.cpp

## Purpose
Provides file I/O utilities for the Autorun tool, including file existence checks and debug logging.

## Responsibilities
- File existence checking (HD/CD paths)
- Debug message logging
- Basic file operations (open/close/read/write)

## Key Types
- StandardFileClass (Class): File I/O wrapper
- None (other types)

## Key Functions
### Full_Path_File_Exists
- Purpose: Check if a file exists at a given path
- Calls: Open_File, Close_File

### HD_File_Exists
- Purpose: Check if a file exists in the HD path
- Calls: Open_File, Close_File

### CD_File_Exists
- Purpose: Check if a file exists in the CD path
- Calls: Open_File, Close_File

### Msg
- Purpose: Write debug messages to file and OutputDebugString
- Calls: StandardFileClass::Open, StandardFileClass::Write, OutputDebugString

### Delete_Msg_File
- Purpose: Delete and recreate the debug log file
- Calls: DeleteFile, StandardFileClass::Open, StandardFileClass::Write

## Globals
- HD_Path (char[MAX_PATH]): Hard drive path prefix
- CD_Path (char[MAX_PATH]): CD-ROM path prefix
- DebugFile (char[MAX_PATH]): Debug log file path

## Dependencies
- windows.h, stdio.h, sys/stat.h
- wnd_file.h, winfix.h
- StandardFileClass (defined in wnd_file.h)
