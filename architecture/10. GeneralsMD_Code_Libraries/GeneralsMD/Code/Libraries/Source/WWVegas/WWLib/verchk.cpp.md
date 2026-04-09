# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/verchk.cpp

## Purpose
Provides utility functions for retrieving version information and file headers from executable files.

## Responsibilities
- Retrieve version information from file version resources
- Get file creation timestamps
- Read PE file headers (DOS and IMAGE_FILE_HEADER)
- Compare executable versions via timestamps

## Key Types
- `IMAGE_FILE_HEADER` (struct): PE file header structure
- `VS_FIXEDFILEINFO` (struct): Windows version info structure
- `FILETIME` (struct): Windows file time structure

## Key Functions
### GetVersionInfo
- Purpose: Retrieves version info from a file's version resource
- Calls: `GetFileVersionInfoSize`, `GlobalAlloc`, `GlobalLock`, `GetFileVersionInfo`, `VerQueryValue`, `GlobalUnlock`, `GlobalFree`

### GetFileCreationTime
- Purpose: Gets the creation time of a file
- Calls: `_TheFileFactory->Get_File`, `file->Open`, `file->Get_File_Handle`, `GetFileTime`, `_TheFileFactory->Return_File`

### Get_Image_File_Header (filename version)
- Purpose: Reads PE file header from a file
- Calls: `_TheFileFactory->Get_File`, `file->Open`, `file->Read`, `file->Seek`, `_TheFileFactory->Return_File`

### Get_Image_File_Header (HINSTANCE version)
- Purpose: Reads PE file header from a loaded module
- Calls: None (direct memory access)

### Compare_EXE_Version
- Purpose: Compares two executables by their timestamps
- Calls: `Get_Image_File_Header` (both versions)

## Globals
- None

## Dependencies
- `verchk.h`, `windows.h`, `winnt.h`, `rawfile.h`, `ffactory.h`
- Windows API: `GetFileVersionInfoSize`, `GetFileVersionInfo`, `VerQueryValue`, `GlobalAlloc`, `GlobalLock`, `GlobalUnlock`, `GlobalFree`, `GetFileTime`
- External symbols: `_TheFileFactory`, `FileClass` methods
