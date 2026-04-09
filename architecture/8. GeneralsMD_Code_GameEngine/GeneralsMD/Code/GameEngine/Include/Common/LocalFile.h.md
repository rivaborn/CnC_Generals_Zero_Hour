# GeneralsMD/Code/GameEngine/Include/Common/LocalFile.h

## Purpose
Defines the LocalFile class, a file abstraction for standard C file operations.

## Responsibilities
- Provides file I/O operations (open, close, read, write, seek)
- Supports line-based and formatted reading (nextLine, scanInt, scanReal, scanString)
- Offers optimized bulk reading (readEntireAndClose)
- Implements memory pool management for instances
- Converts to RAM-based file representation

## Key Types
- **LocalFile (Class)**: File abstraction for standard C file operators.
- **LocalFileMagicEnum (Enum)**: Not inferable (empty definition).
- **LocalFile_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (empty definition).

## Key Functions
### LocalFile()
- Purpose: Constructor for LocalFile.
- Calls: Not inferable.

### open()
- Purpose: Opens a file for access.
- Calls: Not inferable.

### close()
- Purpose: Closes the file.
- Calls: Not inferable.

### read()
- Purpose: Reads bytes into a buffer.
- Calls: Not inferable.

### write()
- Purpose: Writes bytes from a buffer.
- Calls: Not inferable.

### seek()
- Purpose: Sets file position.
- Calls: Not inferable.

### nextLine()
- Purpose: Moves file position to after the next newline.
- Calls: Not inferable.

### scanInt()
- Purpose: Reads an integer at current file position.
- Calls: Not inferable.

### scanReal()
- Purpose: Reads a float at current file position.
- Calls: Not inferable.

### scanString()
- Purpose: Reads a string at current file position.
- Calls: Not inferable.

### readEntireAndClose()
- Purpose: Reads
