# GeneralsMD/Code/GameEngine/Include/Common/XferLoad.h

## Purpose
Defines the XferLoad class for reading data from disk in the SAGE engine's transfer system.

## Responsibilities
- Provides file reading operations for the Xfer system
- Handles block-based reading and skipping
- Manages snapshot loading
- Implements string transfer methods

## Key Types
- **XferLoad (Class)**: Disk read implementation for the Xfer system
- **Snapshot (Class)**: Forward reference to snapshot data structure

## Key Functions
### XferLoad::open
- Purpose: Opens a file for reading
- Calls: Not inferable

### XferLoad::xferSnapshot
- Purpose: Entry point for loading a snapshot from disk
- Calls: Not inferable

### XferLoad::xferImplementation
- Purpose: Core implementation for reading binary data
- Calls: Not inferable

## Globals
- **m_fileFP (FILE*)**: File pointer for the currently open file

## Dependencies
- `<stdio.h>` for file operations
- `Common/Xfer.h` for base Xfer class
- `AsciiString` and `UnicodeString` types
- `Snapshot` class (forward declared)
