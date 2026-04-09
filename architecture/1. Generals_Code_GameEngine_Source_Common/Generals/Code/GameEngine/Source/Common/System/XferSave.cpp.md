# Generals/Code/GameEngine/Source/Common/System/XferSave.cpp

## Purpose
This file implements the `XferSave` class, responsible for saving game data to disk in a structured format.

## Responsibilities
- Manages file opening and closing.
- Handles writing data blocks with size placeholders.
- Supports skipping bytes in the file.
- Transfers snapshots of game state.
- Writes ASCII and Unicode strings.

## Key Types
- **XferBlockData (Class)**: Stores file position and next block pointer for managing data blocks.
- **XferBlockDataMagicEnum (Enum)**: Not inferable from provided context.
- **XferBlockData_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable from provided context.

## Key Functions
### XferSave::XferSave
- Purpose: Initializes the `XferSave` object with default values.
- Calls: None

### XferSave::~XferSave
- Purpose: Cleans up resources, including closing open files and deleting block stack data.
- Calls: `close()`, `deleteInstance()`

### XferSave::open
- Purpose: Opens a file for writing.
- Calls: `fopen()`, `DEBUG_CRASH()`

### XferSave::close
- Purpose: Closes the currently open file.
- Calls: `fclose()`, `clear()`

### XferSave::beginBlock
- Purpose: Writes a placeholder for block size and stores the current file position.
- Calls: `ftell()`, `fwrite()`, `newInstance()`

### XferSave::endBlock
- Purpose: Calculates and writes the actual block size, then restores the file pointer.
- Calls: `ftell()`, `fseek()`, `fwrite()`, `deleteInstance()`

### XferSave::skip
- Purpose: Skips a specified number of bytes in the file.
- Calls: `fseek()`

### XferSave::xferSnapshot
- Purpose: Transfers a snapshot object to the file.
- Calls: `snapshot->xfer(this)`

### XferSave::xferAsciiString
- Purpose: Writes an ASCII string with its length header.
- Calls: `xferUnsignedByte()`, `xferUser()`

### XferSave::xferUnicodeString
- Purpose: Writes a Unicode string with its length header.
- Calls: `xferUnsignedByte()`, `xferUser()`

### XferSave::xferImplementation
- Purpose: Writes raw data to the file.
- Calls: `fwrite()`, `DEBUG_CRASH()`

## Globals
- None

## Dependencies
- **Includes**: "PreRTS.h", "Common/XferSave.h", "Common/Snapshot.h", "Common/GameMemory.h"
- **External Symbols**: `fopen()`, `fclose()`, `ftell()`, `fwrite()`, `f
