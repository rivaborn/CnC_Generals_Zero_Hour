# Generals/Code/Libraries/Source/WWVegas/WWLib/verchk.cpp

## Purpose
Provides utility functions for retrieving version information and file headers from executable files.

## Responsibilities
- Retrieve version information from file version resources
- Get file creation timestamps
- Read PE/COFF file headers from executables
- Compare executable versions by timestamp

## Key Types
- `VS_FIXEDFILEINFO` (struct): Windows version info structure
- `IMAGE_FILE_HEADER` (struct): PE/COFF file header structure
- `IMAGE_DOS_HEADER` (struct): DOS header structure

## Key Functions
### GetVersionInfo
- Purpose: Retrieves version information from a file's version resource
- Calls: `GetFileVersionInfoSize`, `GlobalAlloc`, `GlobalLock`, `GetFileVersionInfo`, `VerQueryValue`, `GlobalUnlock`, `GlobalFree`

### GetFileCreationTime
- Purpose: Gets the creation time of a file
- Calls: `_TheFileFactory->Get_File`, `file->Open`, `file->Get_File_Handle`, `GetFileTime`

### Get_Image_File_Header (filename version)
- Purpose: Reads the PE/COFF file header from an executable file
- Calls: `_TheFileFactory->Get_File`, `file->Open`, `file->Read`, `file->Seek`, `_TheFileFactory->Return_File`

### Get_Image_File_Header (HINSTANCE version)
- Purpose: Reads the PE/COFF file header from a loaded module
- Calls: `memcpy`

### Compare_EXE_Version
- Purpose: Compares two executable versions by their timestamp
- Calls: `Get_Image_File_Header`

## Globals
- None

## Dependencies
- `verchk.h`
- `windows.h`
- `winnt.h`
- `rawfile.h`
- `ffactory.h`
- Windows API: `GetFileVersionInfoSize`, `GetFileVersionInfo`, `VerQueryValue`, `GlobalAlloc`, `GlobalLock`, `GlobalUnlock`, `GlobalFree`, `GetFileTime`
