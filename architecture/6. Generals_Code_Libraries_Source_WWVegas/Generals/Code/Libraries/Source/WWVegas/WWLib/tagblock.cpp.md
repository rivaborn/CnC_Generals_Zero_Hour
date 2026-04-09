# Generals/Code/Libraries/Source/WWVegas/WWLib/tagblock.cpp

## Purpose
Manages tag-based file storage system for game assets, providing indexed access to tagged blocks of data.

## Responsibilities
- Creates and maintains tag block files with indexed access
- Handles opening/creating/closing tag blocks
- Manages file handles and memory indices
- Provides CRC-based lookup for tags
- Handles file header management and validation

## Key Types
- TagBlockIndex (Class): Stores index information for a tag block (CRC, offsets)
- TagBlockFile (Class): Main file class managing tag blocks and indices
- TagBlockHandle (Class): Provides read/write access to a specific tag block
- BlockHeader (Struct): Header information for each tag block

## Key Functions
### TagBlockFile::TagBlockFile
- Purpose: Constructor that opens/creates a tag file and builds index
- Calls: Open, Read, Create_Index, Seek, Calc_Tag_Offset

### TagBlockFile::Create_Tag
- Purpose: Creates a new tag block at the end of the file
- Calls: Create_Index, Seek, Write, W3DNEW

### TagBlockFile::Find_Block
- Purpose: Finds a tag block by name using CRC-based search
- Calls: CRC_Stringi, Seek, Read, strcmpi

### TagBlockHandle::Write
- Purpose: Writes data to a tag block
- Calls: File->Seek, File->Write

### TagBlockHandle::Read
- Purpose: Reads data from a tag block
- Calls: File->Seek, File->Read

## Globals
- TagBlockHandle::_InDestructor (int): Tracks if destructor is being called

## Dependencies
- tagblock.h (header file)
- realcrc.h (for CRC functions)
- RawFileClass (base file class)
- SLNode (linked list node)
- W3DNEW (memory allocation)
- assert.h (for assertions)
