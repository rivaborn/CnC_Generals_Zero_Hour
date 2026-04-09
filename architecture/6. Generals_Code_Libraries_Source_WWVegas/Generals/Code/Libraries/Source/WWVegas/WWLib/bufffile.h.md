# Generals/Code/Libraries/Source/WWVegas/WWLib/bufffile.h

## Purpose
Defines a buffered file I/O class for efficient reading/writing operations.

## Responsibilities
- Provides buffered file operations (read/write/seek/close)
- Manages internal buffer for performance optimization
- Supports both file-based and memory-based operations
- Handles buffer reset and size configuration

## Key Types
- **BufferedFileClass (Class)**: Buffered file I/O wrapper extending RawFileClass
- **BASECLASS (Class)**: Typedef for RawFileClass (base class)

## Key Functions
### BufferedFileClass (constructors)
- Purpose: Initialize buffered file with filename, default, or copy semantics
- Calls: BASECLASS constructors

### operator=
- Purpose: Assign one BufferedFileClass to another
- Calls: BASECLASS assignment

### ~BufferedFileClass
- Purpose: Clean up buffered file resources
- Calls: BASECLASS destructor

### Read
- Purpose: Read data with buffering optimization
- Calls: Not inferable

### Seek
- Purpose: Move file pointer with buffer state management
- Calls: Not inferable

### Write
- Purpose: Write data to file
- Calls: Not inferable

### Close
- Purpose: Close file and release buffer
- Calls: Not inferable

### Reset_Buffer
- Purpose: Clear and reset internal buffer state
- Calls: Not inferable

### Set_Desired_Buffer_Size
- Purpose: Configure default buffer size for all instances
- Calls: None

## Globals
- **_DesiredBufferSize (static int)**: Default buffer size for all BufferedFileClass instances

## Dependencies
- **rawfile.h**: Base RawFileClass definition
- **RawFileClass**: Base class for file operations
