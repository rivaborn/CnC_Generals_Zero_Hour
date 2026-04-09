# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/rcfile.h

## Purpose
Defines the `ResourceFileClass` for reading binary files embedded as Windows resources.

## Responsibilities
- Wraps resource-based file I/O
- Provides read-only access to embedded files
- Manages resource module and memory pointers

## Key Types
- **ResourceFileClass (Class)**: Handles resource-based file operations

## Key Functions
### ResourceFileClass::ResourceFileClass
- Purpose: Constructs a resource file handle
- Calls: Not inferable

### ResourceFileClass::Read
- Purpose: Reads data from the embedded resource
- Calls: Not inferable

### ResourceFileClass::Seek
- Purpose: Changes the read position in the resource
- Calls: Not inferable

### ResourceFileClass::Size
- Purpose: Returns the size of the embedded resource
- Calls: Not inferable

### ResourceFileClass::Error
- Purpose: Handles resource access errors
- Calls: Not inferable

## Globals
- None

## Dependencies
- `always.h`, `wwfile.h`, `win.h`
- `FileClass` (base class)
- Windows API (`HMODULE`)
