# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/tagblock.cpp

## Purpose
Manages tag-based file storage system for game assets, handling creation, indexing, and retrieval of tagged data blocks.

## Responsibilities
- Manages tag block file I/O operations
- Maintains in-memory index of tags sorted by CRC
- Handles tag creation, opening, and closing
- Provides handle-based access to tag data
- Ensures file integrity and proper cleanup

## Key Types
- **TagBlockIndex (Class)**: Stores metadata about a tag block (CRC, offsets, size)
- **TagBlockFile (Class)**: Manages the tag file and its index
- **TagBlockHandle (Class)**: Provides read/write access to a specific tag block
- **BlockHeader (Struct)**: Header information for each tag block

## Key Functions
### TagBlockFile::TagBlockFile
- Purpose: Constructor that opens/creates a tag file and builds index
- Calls: Open, Read, Create_Index, Calc_Data_Offset, Calc_Tag_Offset

### TagBlockFile::Create_Tag
- Purpose: Creates a new tag block in the file
- Calls: Create_Index, Seek, Write

### TagBlockHandle::Write
- Purpose: Writes data to a tag block
- Calls: File->Seek, File->Write

### TagBlockFile::Find_Block
- Purpose: Finds a tag block by name using CRC-based search
- Calls: CRC_Stringi, Seek, Read, strcmpi

### TagBlockFile::End_Write_Access
- Purpose: Finalizes a tag block after writing
- Calls: Seek, Write, Save_Header

## Globals
- **TagBlockHandle::_InDestructor (int)**: Tracks if destructor is active

## Dependencies
- tagblock.h (header)
- realcrc.h (for CRC functions)
- RawFileClass (base class)
- SLNode (for linked list)
- W3DNEW (memory allocation)
- assert.h (for assertions)
