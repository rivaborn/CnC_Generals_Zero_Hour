# GeneralsMD/Code/GameEngine/Source/Common/System/XferSave.cpp

## Purpose
Implements disk write functionality for save/load operations in the game engine.

## Responsibilities
- Manages file I/O for save operations
- Handles block-based file structure (begin/end blocks)
- Serializes game data (strings, snapshots) to disk
- Tracks file positions and block sizes

## Key Types
- **XferBlockData (Class)**: Tracks file position and next block in a linked list for block management.
- **XferBlockDataMagicEnum (Enum)**: Not inferable (likely unused placeholder).
- **XferBlockData_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely unused placeholder).

## Key Functions
### `XferSave::open`
- Purpose: Opens a file for writing.
- Calls: `Xfer::open`, `fopen`, `DEBUG_CRASH`.

### `XferSave::close`
- Purpose: Closes the current file.
- Calls: `fclose`, `DEBUG_CRASH`.

### `XferSave::beginBlock`
- Purpose: Writes a placeholder for a block and saves its position.
- Calls: `ftell`, `fwrite`, `newInstance`, `DEBUG_CRASH`.

### `XferSave::endBlock`
- Purpose: Finalizes a block by writing its size and restoring file position.
- Calls: `ftell`, `fseek`, `fwrite`, `deleteInstance`, `DEBUG_CRASH`.

### `XferSave::xferSnapshot`
- Purpose: Serializes a snapshot object to disk.
- Calls: `DEBUG_CRASH`, `Snapshot::xfer`.

### `XferSave::xferAsciiString`
- Purpose: Writes an ASCII string to the file.
- Calls: `xferUnsignedByte`, `xferUser`, `DEBUG_CRASH`.

### `XferSave::xferUnicodeString`
- Purpose: Writes a Unicode string to the file.
- Calls: `xferUnsignedByte`, `xferUser`, `DEBUG_CRASH`.

### `XferSave::xferImplementation`
- Purpose: Low-level write operation for raw data.
- Calls: `fwrite`, `DEBUG_CRASH`.

## Globals
- **m_fileFP (FILE**)**: File pointer for the open file.
- **m_blockStack (XferBlockData**)**: Stack of block descriptors for nested blocks.
- **m_identifier (AsciiString)**: Name of the currently open file.

## Dependencies
- `PreRTS.h`, `Common/XferSave.h`, `Common/Snapshot.h`, `Common/GameMemory.h`
- `fopen`, `fclose`, `fwrite`, `ftell`, `fseek` (C stdio
