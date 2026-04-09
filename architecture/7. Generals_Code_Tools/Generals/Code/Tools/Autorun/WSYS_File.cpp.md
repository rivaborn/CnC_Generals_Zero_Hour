# Generals/Code/Tools/Autorun/WSYS_File.cpp

## Purpose
Implements the base `File` class for the WSYS library, providing core file I/O functionality.

## Responsibilities
- Manages file state (open/close, access mode)
- Provides basic file operations (read/write, seek, size)
- Handles file naming and formatting
- Supports text and binary modes
- Implements self-deletion on close (special case)

## Key Types
- `File` (Class): Base file abstraction with core I/O operations
- `Bool` (Type): Boolean type (TRUE/FALSE)
- `Char` (Type): Character type
- `Int` (Type): Integer type
- `UnsignedInt` (Type): Unsigned integer type

## Key Functions
### `File::open`
- Purpose: Opens a file with specified access mode
- Calls: `setName`

### `File::close`
- Purpose: Closes the file and optionally deletes the object
- Calls: `setName`

### `File::size`
- Purpose: Returns the file size by seeking
- Calls: `seek`

### `File::position`
- Purpose: Returns current file position
- Calls: `seek`

### `File::printf`
- Purpose: Formats and writes text to the file
- Calls: `write`, `vsprintf`

## Globals
- None

## Dependencies
- `<assert.h>`, `<string.h>`, `<stdarg.h>`, `<stdio.h>`
- `wsys_File.h` (header for `File` class)
- External symbols: `vsprintf`, `strlen`, `strcpy`, `strncpy`
