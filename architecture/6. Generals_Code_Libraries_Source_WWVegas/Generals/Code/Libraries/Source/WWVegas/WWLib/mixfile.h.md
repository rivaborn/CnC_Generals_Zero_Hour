# Generals/Code/Libraries/Source/WWVegas/WWLib/mixfile.h

## Purpose
Defines classes for managing MIX file archives (packed file containers) in the game engine.

## Responsibilities
- Provides MIX file factory for loading/saving files from archives
- Supports adding/deleting files in MIX archives
- Manages filename lists and file information
- Handles MIX file creation and modification

## Key Types
- **MixFileFactoryClass (Class)**: Manages MIX file archives, loading/saving files
- **MixFileCreator (Class)**: Creates new MIX archives and adds files to them
- **FileInfoStruct (Struct)**: Stores file metadata (CRC, offset, size)
- **AddInfoStruct (Struct)**: Tracks pending file additions
- **FileClass (Class)**: Base file class (defined elsewhere)

## Key Functions
### Setup_Mix_File
- Purpose: Initializes MIX file system
- Calls: Not inferable

### MixFileFactoryClass::Get_File
- Purpose: Retrieves a file from the MIX archive
- Calls: Not inferable

### MixFileFactoryClass::Add_File
- Purpose: Adds a file to the MIX archive
- Calls: Get_Temp_Filename

### MixFileCreator::Add_File
- Purpose: Adds files to a MIX archive being created
- Calls: Not inferable

## Globals
- None

## Dependencies
- `always.h`, `ffactory.h`, `wwstring.h`, `vector.h`
- `FileClass`, `FileFactoryClass`, `StringClass`, `DynamicVectorClass`
