# Generals/Code/Libraries/Source/WWVegas/WWLib/WWFILE.H

## Purpose
Defines the abstract `FileClass` interface for file I/O operations in the SAGE engine.

## Responsibilities
- Declares virtual methods for file operations (open, read, write, seek, etc.)
- Provides macros for parsing date/time values from file timestamps
- Defines seek constants (`SEEK_SET`, `SEEK_CUR`, `SEEK_END`)
- Includes `printf`-style formatted output methods for files

## Key Types
- **FileClass (Class)**: Abstract base class for file operations.
- **FileClass::READ (Enum)**: Flag for read-only file access.
- **FileClass::WRITE (Enum)**: Flag for write-only file access.
- **FileClass::PRINTF_BUFFER_SIZE (Enum)**: Default buffer size for `Printf` operations.

## Key Functions
### `FileClass::Printf`
- Purpose: Writes formatted text to the file using a stack buffer.
- Calls: Not inferable (uses variadic arguments).

### `FileClass::Printf` (buffered version)
- Purpose: Writes formatted text to the file using a user-supplied buffer.
- Calls: Not inferable (uses variadic arguments).

### `FileClass::Printf_Indented`
- Purpose: Writes formatted text with leading tabs for indentation.
- Calls: Not inferable (uses variadic arguments).

## Globals
- **YEAR(dt) (Macro)**: Extracts year from a file timestamp.
- **MONTH(dt) (Macro)**: Extracts month from a file timestamp.
- **DAY(dt) (Macro)**: Extracts day from a file timestamp.
- **HOUR(dt) (Macro)**: Extracts hour from a file timestamp.
- **MINUTE(dt) (Macro)**: Extracts minute from a file
