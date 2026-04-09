# Generals/Code/Libraries/Source/WWVegas/WWLib/rcfile.h

## Purpose
Defines a resource-based file class for reading binary data embedded as Windows resources.

## Responsibilities
- Wraps Windows resources as a file-like interface
- Provides read-only access to embedded binary data
- Manages resource loading and memory pointers

## Key Types
- **ResourceFileClass (Class)**: Wrapper for accessing binary data stored as Windows resources

## Key Functions
### ResourceFileClass::ResourceFileClass
- Purpose: Constructs a resource file handle from a module and resource name
- Calls: Not inferable

### ResourceFileClass::Read
- Purpose: Reads data from the embedded resource
- Calls: Not inferable

### ResourceFileClass::Seek
- Purpose: Moves the read pointer within the resource data
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
- Inherits from `FileClass`
- Uses Windows API types (`HMODULE`)
