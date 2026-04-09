# Generals/Code/Libraries/Source/WWVegas/WWLib/TagBlock.h

## Purpose
Defines the TagBlockFile and TagBlockHandle classes for managing tagged variable-size blocks in a file, supporting write-once/read-many access.

## Responsibilities
- Manages file-based storage of named data blocks
- Provides read/write access via handles
- Maintains file integrity with headers and indexing
- Supports block creation, opening, and closing

## Key Types
- **TagBlockFile (Class)**: Main file management class
- **TagBlockHandle (Class)**: Handle for accessing blocks
- **FileHeader (Struct)**: File metadata (version, block count, size)
- **BlockHeader (Struct)**: Per-block metadata (index, tag size, data size)
- **TagBlockIndex (Class)**: Index entry for block lookup

## Key Functions
### TagBlockFile::Open_Tag
- Purpose: Opens an existing block for reading
- Calls: Find_Block

### TagBlockFile::Create_Tag
- Purpose: Creates a new writable block
- Calls: None visible

### TagBlockHandle::Write
- Purpose: Writes data to the block
- Calls: None visible

### TagBlockHandle::End_Write_Access
- Purpose: Finalizes write access and flushes data
- Calls: File->End_Write_Access

## Globals
- **_InDestructor (int)**: Flag to prevent double destruction

## Dependencies
- **slist.h**: For SList<TagBlockIndex>
- **crc.h**: For CRC calculations
- **rawfile.h**: Base file I/O class
- **string.h**: For memset/memcpy
