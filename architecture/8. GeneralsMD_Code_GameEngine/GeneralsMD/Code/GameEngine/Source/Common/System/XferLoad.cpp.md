# GeneralsMD/Code/GameEngine/Source/Common/System/XferLoad.cpp

## Purpose
Implements file-based loading functionality for the Xfer (transfer) system, handling binary data reads from disk.

## Responsibilities
- Opens/closes files for reading
- Reads binary data blocks and primitive types
- Handles string serialization (ASCII/Unicode)
- Manages snapshot loading and post-processing
- Provides error handling for file operations

## Key Types
- `XferLoad` (Class): File-based data loader implementation
- `XferBlockSize` (Type): Block size descriptor for file reads

## Key Functions
### `open`
- Purpose: Opens a file for reading
- Calls: `Xfer::open`, `fopen`

### `close`
- Purpose: Closes the currently open file
- Calls: `fclose`

### `beginBlock`
- Purpose: Reads a block size descriptor from the file
- Calls: `fread`

### `skip`
- Purpose: Skips forward in the file by specified bytes
- Calls: `fseek`

### `xferSnapshot`
- Purpose: Loads a snapshot from file and adds it to game state
- Calls: `Snapshot::xfer`, `TheGameState->addPostProcessSnapshot`

### `xferAsciiString`
- Purpose: Reads an ASCII string from file
- Calls: `xferUnsignedByte`, `xferUser`

### `xferUnicodeString`
- Purpose: Reads a Unicode string from file
- Calls: `xferUnsignedByte`, `xferUser`

### `xferImplementation`
- Purpose: Core read operation for binary data
- Calls: `fread`

## Globals
- `MAX_XFER_LOAD_STRING_BUFFER` (const Int): Buffer size for string operations

## Dependencies
- `PreRTS.h`, `Common/Debug.h`, `Common/GameState.h`, `Common/Snapshot.h`, `Common/XferLoad.h`
- `Xfer` base class
- `Snapshot` class
- Standard C file I/O (`fopen`, `fread`, `fseek`, `fclose`)
- `AsciiString`, `UnicodeString` classes
