# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/mixfile.h

## Purpose
Defines classes for handling mix files (archive files) in the game engine, including file management and creation.

## Responsibilities
- Manage mix file archives (packed resource files)
- Provide file access and modification capabilities
- Support building filename lists and file operations
- Handle file addition/deletion and CRC tracking
- Create new mix files from source files

## Key Types
- **MixFileFactoryClass (Class)**: Manages mix file archives, file access, and modifications.
- **MixFileCreator (Class)**: Creates new mix files by adding source files.
- **FileInfoStruct (Struct)**: Stores file metadata (CRC, offset, size).
- **AddInfoStruct (Struct)**: Tracks pending file additions (full path, filename).
- **FileClass (Class)**: Base file class (external dependency).

## Key Functions
### Setup_Mix_File
- Purpose: Initializes mix file system.
- Calls: Not inferable.

### MixFileFactoryClass::Get_File
- Purpose: Retrieves a file from the mix archive.
- Calls: Not inferable.

### MixFileFactoryClass::Add_File
- Purpose: Adds a file to the mix archive.
- Calls: Not inferable.

### MixFileCreator::Add_File
- Purpose: Adds a file to a mix file being created.
- Calls: Not inferable.

## Globals
- None.

## Dependencies
- `always.h`, `ffactory.h`, `wwstring.h`, `vector.h`
- `FileClass`, `FileFactoryClass`, `StringClass`, `DynamicVectorClass`
