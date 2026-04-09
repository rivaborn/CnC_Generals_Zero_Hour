# Generals/Code/Tools/Babylon/iff.h

## Purpose
Header file defining IFF (Interchange File Format) file handling structures and functions for reading/writing IFF-formatted files.

## Responsibilities
- Defines IFF file and chunk structures
- Provides IFF file I/O functions
- Includes endianness conversion macros
- Declares helper macros for error handling

## Key Types
- IFF_CHUNK (struct): Represents an IFF chunk with ID and size
- IFF_FILE (struct): Main IFF file structure tracking file state and position
- (anonymous structs): Not directly used, likely internal implementation details

## Key Functions
### IFF_Open
- Purpose: Opens an IFF file for reading
- Calls: Not inferable

### IFF_Load
- Purpose: Loads an entire IFF file into memory
- Calls: Not inferable

### IFF_Read / IFF_Write
- Purpose: Reads/writes data from/to IFF file
- Calls: Not inferable

### IFF_NewForm / IFF_NewChunk
- Purpose: Creates new form/chunk in IFF file
- Calls: Not inferable

## Globals
- None

## Dependencies
- Uses `open`, `read`, `write` system calls
- References `W_MakeID` (not defined here)
- Uses `VOID` type (not defined here)
