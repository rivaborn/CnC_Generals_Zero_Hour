# GeneralsMD/Code/GameEngine/Include/Common/StreamingArchiveFile.h

## Purpose
Defines a file abstraction class for streaming file operations, inheriting from RAMFile.

## Responsibilities
- Provides streaming file I/O operations (open, close, read, write, seek)
- Manages file position and size tracking
- Disables INI-style parsing methods (nextLine, scanInt, etc.) for streaming files
- Supports opening files from archives or directly from the filesystem

## Key Types
- **StreamingArchiveFile (Class)**: File abstraction for streaming operations.
- **StreamingArchiveFileMagicEnum (Enum)**: Not inferable (empty definition).
- **StreamingArchiveFile_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (empty definition).

## Key Functions
### StreamingArchiveFile::open
- Purpose: Opens a file for streaming access.
- Calls: Not inferable (implementation not shown).

### StreamingArchiveFile::read
- Purpose: Reads bytes from the file into a buffer.
- Calls: Not inferable.

### StreamingArchiveFile::write
- Purpose: Writes bytes from a buffer to the file.
- Calls: Not inferable.

### StreamingArchiveFile::seek
- Purpose: Sets the file position.
- Calls: Not inferable.

### StreamingArchiveFile::openFromArchive
- Purpose: Opens a file from an archive at a given offset and size.
- Calls: Not inferable.

## Globals
- **None**

## Dependencies
- **RAMFile.h**: Base class for file operations.
- **File**: External class for file handling (used as member variable).
- **AsciiString**: Used for filename parameter in `openFromArchive`.
- **DEBUG_CRASH**: Macro for runtime assertions (used in disabled methods).
