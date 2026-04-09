# Generals/Code/Libraries/Source/WWVegas/WWLib/RAMFILE.H

## Purpose
Defines a RAM-based file abstraction for in-memory file operations.

## Responsibilities
- Provides a FileClass-derived interface for memory buffers
- Supports read/write operations on allocated or external buffers
- Manages file position, size, and access mode
- Handles buffer allocation/deallocation lifecycle

## Key Types
- RAMFileClass (Class): In-memory file implementation using a buffer

## Key Functions
### RAMFileClass constructor
- Purpose: Initializes the RAM file with a buffer and length
- Calls: None

### Open
- Purpose: Opens the RAM file in specified access mode
- Calls: None

### Read
- Purpose: Reads data from the buffer at current position
- Calls: None

### Write
- Purpose: Writes data to the buffer at current position
- Calls: None

### Seek
- Purpose: Changes the current file position within the buffer
- Calls: None

### Close
- Purpose: Closes the RAM file
- Calls: None

## Globals
- None

## Dependencies
- Key includes: "wwfile.h"
- External symbols: FileClass (base class)
