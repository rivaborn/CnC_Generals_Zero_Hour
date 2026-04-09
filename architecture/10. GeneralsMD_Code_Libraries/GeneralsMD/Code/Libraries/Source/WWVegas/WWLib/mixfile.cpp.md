# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/mixfile.cpp

## Purpose
Handles creation, modification, and access of MIX (mixed) archive files used for bundling game assets.

## Responsibilities
- Manages MIX file headers and data structures
- Provides file factory for reading/writing MIX archives
- Supports adding/deleting files and flushing changes
- Implements CRC-based file lookup and ordering

## Key Types
- **MIXFILE_HEADER (Class)**: Contains MIX file signature and offset pointers
- **MIXFILE_DATA_HEADER (Class)**: Stores file count in MIX data section
- **FileOffsetStruct (Class)**: Associates filenames with their offsets
- **MixFileFactoryClass (Class)**: Main factory for MIX file operations
- **MixFileCreator (Class)**: Handles creation of new MIX files

## Key Functions
### Add_Files
- Purpose: Recursively adds files from directory to MIX file
- Calls: `MixFileCreator::Add_File`, `FindFirstFile`, `FindNextFile`

### Setup_Mix_File
- Purpose: Initializes MIX file creation process
- Calls: `Add_Files`, `MixFileCreator` constructor

### MixFileFactoryClass::Get_File
- Purpose: Retrieves a file from MIX archive by CRC
- Calls: `CRC_Stringi`, binary search on `FileInfo`

### MixFileCreator::Add_File
- Purpose: Adds a file to MIX archive with CRC indexing
- Calls: `_SimpleFileFactory.Get_File`, `MixFile->Write`

## Globals
- **_SimpleFileFactory (SimpleFileFactoryClass)**: Global file factory instance

## Dependencies
- `mixfile.h`, `wwdebug.h`, `ffactory.h`, `wwfile.h`, `realcrc.h`, `rawfile.h`, `win.h`, `bittype.h`
- `FileClass`, `StringClass`, `DynamicVectorClass`, `RawFileClass`
