# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/RAMFILE.H

## Purpose
Defines the RAMFileClass, a memory-based file implementation for the SAGE engine.

## Responsibilities
- Provides in-memory file operations (read/write/seek)
- Manages a buffer as a virtual file
- Implements FileClass interface for memory-based storage
- Handles file position tracking and access modes

## Key Types
- RAMFileClass (Class): In-memory file implementation inheriting from FileClass

## Key Functions
### RAMFileClass constructor
- Purpose: Initializes the RAM file with a buffer and length
- Calls: None

### Open
- Purpose: Opens the RAM file in specified access mode
- Calls: None

### Read
- Purpose: Reads data from the RAM file buffer
- Calls: None

### Write
- Purpose: Writes data to the RAM file buffer
- Calls: None

### Seek
- Purpose: Changes the current position within the RAM file
- Calls: None

### Size
- Purpose: Returns the size of the RAM file
- Calls: None

### Close
- Purpose: Closes the RAM file
- Calls: None

### Bias
- Purpose: Adjusts the file position with optional length constraint
- Calls: None

## Globals
- None

## Dependencies
- Key includes: "wwfile.h"
- External symbols: FileClass (base class)
