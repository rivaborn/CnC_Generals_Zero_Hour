# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/TagBlock.h

## Purpose
Defines the TagBlockFile and TagBlockHandle classes for managing tagged variable-size blocks in a file, supporting write-once/read-many operations.

## Responsibilities
- Manages file-based storage of named data blocks
- Provides read/write access via handles
- Maintains file integrity and indexing
- Supports block creation and lookup

## Key Types
- **TagBlockFile (Class)**: Main file management class
- **TagBlockHandle (Class)**: Handle for accessing blocks
- **TagBlockIndex (Class)**: Index entry for block lookup
- **FileHeader (Struct)**: File metadata structure
- **BlockHeader (Struct)**: Per-block metadata structure
- **FILE_VERSION (Enum)**: File format version constant
- **MAX_TAG_NAME_SIZE (Enum)**: Maximum tag name length

## Key Functions
### TagBlockFile::Open_Tag
- Purpose: Opens an existing tag for reading
- Calls: Find_Block

### TagBlockFile::Create_Tag
- Purpose: Creates a new writable tag
- Calls: Create_Index

### TagBlockHandle::Write
- Purpose: Writes data to the block
- Calls: RawFileClass::Write

### TagBlockHandle::Read
- Purpose: Reads data from the block
- Calls: RawFileClass::Read

### TagBlockFile::Find_Block
- Purpose: Locates a block by tag name
- Calls: None

## Globals
- **_InDestructor (int)**: Flag to prevent double destruction

## Dependencies
- **slist.h**: For SList<TagBlockIndex>
- **crc.h**: For CRC calculations
- **rawfile.h**: Base file I/O class
- **string.h**: For memset/memcpy
