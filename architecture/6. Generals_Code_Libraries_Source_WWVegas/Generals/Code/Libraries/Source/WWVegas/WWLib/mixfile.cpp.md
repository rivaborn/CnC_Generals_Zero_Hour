# Generals/Code/Libraries/Source/WWVegas/WWLib/mixfile.cpp

## Purpose
Handles creation, modification, and access of MIX (mixed) archive files used for bundling game assets.

## Responsibilities
- Manages MIX file headers and data structures
- Implements file addition/deletion/flushing for MIX archives
- Provides file factory interface for MIX archives
- Handles CRC-based file lookup within archives
- Supports recursive directory scanning for batch file addition

## Key Types
- **MIXFILE_HEADER (struct)**: Contains MIX file signature, header offset, and names offset
- **MIXFILE_DATA_HEADER (struct)**: Contains file count in MIX file
- **MixFileFactoryClass (Class)**: Manages reading from existing MIX files
- **MixFileCreator (Class)**: Handles creation of new MIX files
- **FileInfoStruct (struct)**: Stores CRC, offset, size, and filename for archived files

## Key Functions
### `Add_Files`
- Purpose: Recursively scans directories and adds files to a MIX archive
- Calls: `FindFirstFile`, `FindNextFile`, `MixFileCreator::Add_File`

### `Setup_Mix_File`
- Purpose: Initializes MIX file creation process and builds default MAKEMIX.MIX
- Calls: `SimpleFileFactoryClass::Set_Sub_Directory`, `MixFileCreator` constructor, `Add_Files`

## Globals
- **_SimpleFileFactory (SimpleFileFactoryClass)**: Global file factory instance for MIX operations

## Dependencies
- Key includes: `mixfile.h`, `wwdebug.h`, `ffactory.h`, `wwfile.h`, `realcrc.h`, `rawfile.h`, `win.h`, `bittype.h`
- External symbols: `CRC_Stringi`, `qsort`, `GetFileAttributes`, `DeleteFile`, `MoveFile`, `FindFirstFile`, `FindNextFile`
