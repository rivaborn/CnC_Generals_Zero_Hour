# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/BUFF.H

## Purpose
Defines a general-purpose buffer management class for handling memory buffers with size tracking.

## Responsibilities
- Manages buffer memory allocation/deallocation
- Tracks buffer size and validity
- Provides safe buffer access via pointer casting
- Supports buffer copying and resetting

## Key Types
- Buffer (Class): wrapper for buffer memory and size metadata

## Key Functions
### Buffer constructors
- Purpose: Initialize buffer with pointer and size
- Calls: None

### operator= (assignment)
- Purpose: Copy buffer contents from another Buffer
- Calls: None

### Reset
- Purpose: Clear buffer pointer and size
- Calls: None

### Get_Buffer
- Purpose: Return raw buffer pointer
- Calls: None

### Get_Size
- Purpose: Return buffer size
- Calls: None

### Is_Valid
- Purpose: Check if buffer pointer is non-null
- Calls: None

## Globals
- None

## Dependencies
- "bool.h" for bool type definition
- Standard C++ memory management (new/delete)
