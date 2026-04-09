# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/WWFILE.H

## Purpose
Defines the abstract `FileClass` interface for file operations in the SAGE engine.

## Responsibilities
- Declares virtual methods for file I/O (read/write/open/close).
- Provides date/time macros for file metadata.
- Defines `printf`-style output methods for file writing.
- Establishes seek/tell/positioning functionality.

## Key Types
- **FileClass (Class)**: Abstract base class for file operations.
  - **READ/WRITE (Enum)**: File access modes.
  - **PRINTF_BUFFER_SIZE (Const)**: Default buffer size for `printf`.

## Key Functions
### `Printf`
- Purpose: Writes formatted text to the file using a stack buffer.
- Calls: Not inferable (uses variadic arguments).

### `Printf` (buffered)
- Purpose: Writes formatted text to a user-supplied buffer.
- Calls: Not inferable.

### `Printf_Indented`
- Purpose: Writes formatted text with leading tabs for indentation.
- Calls: Not inferable.

## Globals
- **SEEK_SET/SEEK_CUR/SEEK_END (Macros)**: Standard seek modes.
- **YEAR/MONTH/DAY/HOUR/MINUTE/SECOND (Macros)**: Extract date/time from a 32-bit value.

## Dependencies
- `osdep.h` (Unix-specific includes).
- `reinterpret_cast` (for `Get_File_Handle`).
- Variadic argument handling (for `Printf` methods).
