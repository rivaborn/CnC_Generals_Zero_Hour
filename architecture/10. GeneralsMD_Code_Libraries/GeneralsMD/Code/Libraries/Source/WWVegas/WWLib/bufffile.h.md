# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/bufffile.h

## Purpose
Defines a buffered file I/O class for efficient reading/writing operations.

## Responsibilities
- Provides buffered file operations (read/write/seek/close)
- Manages internal buffer allocation and reset
- Supports static buffer size configuration
- Inherits from RawFileClass for base file functionality

## Key Types
- **BufferedFileClass (Class)**: Buffered file I/O wrapper with read/write caching
- **BASECLASS (Class)**: Typedef for RawFileClass (base class)

## Key Functions
### BufferedFileClass (constructors)
- Purpose: Initialize buffered file with filename, default, or copy semantics
- Calls: Not inferable

### operator=
- Purpose: Assign buffered file state from another instance
- Calls: Not inferable

### ~BufferedFileClass
- Purpose: Clean up buffered file resources
- Calls: Not inferable

### Read
- Purpose: Read data with buffering optimization
- Calls: Not inferable

### Seek
- Purpose: Move file pointer with buffering awareness
- Calls: Not inferable

### Write
- Purpose: Write data to file
- Calls: Not inferable

### Close
- Purpose: Close file and release buffer
- Calls: Not inferable

### Set_Desired_Buffer_Size
- Purpose: Configure default buffer size for all instances
- Calls: Not inferable

### Reset_Buffer
- Purpose: Clear or reinitialize read buffer
- Calls: Not inferable

## Globals
- **_DesiredBufferSize (static int)**: Default buffer size for all BufferedFileClass instances

## Dependencies
- **rawfile.h**: Base RawFileClass definition
- **SEEK_CUR**: Standard file seek constant
