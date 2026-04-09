# Generals/Code/Libraries/Source/WWVegas/WWLib/XSTRAW.H

## Purpose
Defines abstract data source classes (Straw) for reading from buffers and files.

## Responsibilities
- Provides `BufferStraw` for reading from memory buffers
- Provides `FileStraw` for reading from files
- Implements `Get()` method for both classes
- Manages buffer/file state and validity

## Key Types
- **BufferStraw (Class)**: Wraps a buffer as a data source
- **FileStraw (Class)**: Wraps a file as a data source
- **Straw (Class)**: Base abstract data source class (external)

## Key Functions
### BufferStraw::Get
- Purpose: Reads data from the internal buffer
- Calls: `BufferPtr.Is_Valid()`

### FileStraw::Get
- Purpose: Reads data from the associated file
- Calls: `Valid_File()`

### FileStraw::~FileStraw
- Purpose: Cleans up file resources
- Calls: Not inferable

## Globals
- None

## Dependencies
- `buff.h` (Buffer class)
- `straw.h` (Straw base class)
- `wwfile.h` (FileClass)
- `<stddef.h>` (size_t)
