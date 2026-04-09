# Generals/Code/GameEngine/Source/Common/System/XferLoad.cpp

## Purpose
This file implements the `XferLoad` class, responsible for loading data from disk in the Command & Conquer Generals game engine.

## Responsibilities
- Open and close files for reading.
- Read blocks of data from a file.
- Skip specified bytes in a file.
- Transfer snapshots and strings from a file to in-memory structures.

## Key Types
- `XferLoad` (Class): Handles loading operations from disk.
- `XferBlockSize` (Type): Represents the size of a block being read.
- `AsciiString` (Class): Stores ASCII strings.
- `UnicodeString` (Class): Stores Unicode strings.

## Key Functions
### XferLoad::open
- Purpose: Opens a file for reading.
- Calls: `fopen`, `Xfer::open`

### XferLoad::close
- Purpose: Closes the currently open file.
- Calls: `fclose`

### XferLoad::beginBlock
- Purpose: Reads the block size from the file.
- Calls: `fread`

### XferLoad::skip
- Purpose: Skips a specified number of bytes in the file.
- Calls: `fseek`

### XferLoad::xferSnapshot
- Purpose: Transfers data from the file into a snapshot object.
- Calls: `snapshot->xfer`, `TheGameState->addPostProcessSnapshot`

### XferLoad::xferAsciiString
- Purpose: Reads an ASCII string from the file.
- Calls: `xferUnsignedByte`, `xferUser`

### XferLoad::xferUnicodeString
- Purpose: Reads a Unicode string from the file.
- Calls: `xferUnsignedByte`, `xferUser`

### XferLoad::xferImplementation
- Purpose: Performs the actual read operation from the file.
- Calls: `fread`

## Globals
- None

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/Debug.h"
  - "Common/GameState.h"
  - "Common/Snapshot.h"
  - "Common/XferLoad.h"

- External symbols used but not defined here:
  - `DEBUG_CRASH`
  - `DEBUG_ASSERTCRASH`
  - `BitTest`
  - `TheGameState`
