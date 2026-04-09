# Generals/Code/Tools/Autorun/EZGIMEX.cpp

## Purpose
Provides low-level file and memory I/O abstractions for the GIMAX library, supporting both Motorola and Intel byte ordering.

## Responsibilities
- Memory allocation/deallocation with tracking
- File stream operations (open, close, read, write, seek)
- Byte order conversion (Motorola/Intel) for binary data
- File length and position queries

## Key Types
- `GSTREAM` (Type): Opaque handle for file streams (typedef'd to `FILE*`)

## Key Functions
### `galloc`
- Purpose: Allocates memory and increments global allocation counter.
- Calls: `malloc`

### `gfree`
- Purpose: Frees memory and decrements global allocation counter.
- Calls: `free`

### `ggetm`
- Purpose: Reads Motorola-format (big-endian) multi-byte values from memory.
- Calls: None

### `ggeti`
- Purpose: Reads Intel-format (little-endian) multi-byte values from memory.
- Calls: None

### `gputm`
- Purpose: Writes Motorola-format (big-endian) multi-byte values to memory.
- Calls: None

### `gputi`
- Purpose: Writes Intel-format (little-endian) multi-byte values to memory.
- Calls: None

### `gopen`
- Purpose: Opens an existing file for read/write access.
- Calls: `fopen`, `Msg`

### `gwopen`
- Purpose: Creates/opens a file for write access.
- Calls: `fopen`

### `gclose`
- Purpose: Closes a file stream.
- Calls: `fclose`

### `gread`
- Purpose: Reads data from a file stream.
- Calls: `fread`

### `gwrite`
- Purpose: Writes data to a file stream.
- Calls: `fwrite`

### `gseek`
- Purpose: Seeks to an absolute position in a file.
- Calls: `fseek`

### `glen`
- Purpose: Returns the length of a file in bytes.
- Calls: `gtell`, `fseek`

### `gtell`
- Purpose: Returns the current position in a file.
- Calls: `ftell`

## Globals
- `galloccount` (int): Tracks number of active memory allocations

## Dependencies
- `<stdlib.h>`, `<string.h>`, `<stdio.h>`
- `gimex.h`, `wnd_file.h`
- `FILE` (from C runtime), `Msg` (logging function)
