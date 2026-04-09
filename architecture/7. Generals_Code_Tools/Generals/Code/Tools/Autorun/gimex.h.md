# Generals/Code/Tools/Autorun/gimex.h

## Purpose
Header file defining the GIMEX (Graphics IMport EXport) API for bitmap manipulation and file I/O operations.

## Responsibilities
- Defines data structures for bitmap info, file streams, and module metadata
- Declares core file I/O and memory management functions
- Provides platform-specific ARGB color structure definitions
- Includes example module prototypes and utility macros

## Key Types
- **ARGB (struct)**: Platform-specific color structure with alpha, red, green, blue channels
- **GINFO (struct)**: Bitmap metadata including dimensions, palette, hotspots, and frame info
- **GSTREAM (typedef)**: Opaque handle for file stream operations
- **GINSTANCE (struct)**: File instance metadata with frame and stream references
- **GABOUT (struct)**: Module capabilities and format information
- **GBITMAP (struct)**: Bitmap data container with pointer to image pixels

## Key Functions
### gopen
- Purpose: Opens a file for reading
- Calls: Not inferable

### gwopen
- Purpose: Opens a file for writing
- Calls: Not inferable

### gread
- Purpose: Reads data from a file stream
- Calls: Not inferable

### gwrite
- Purpose: Writes data to a file stream
- Calls: Not inferable

### galloc
- Purpose: Allocates memory
- Calls: Not inferable

### gfree
- Purpose: Frees allocated memory
- Calls: Not inferable

## Globals
- **GimexVersion (const char*)**: Version string "2.26"
- **GMAKEID (macro)**: Creates 32-bit ID from 4 bytes
- **gmin/gmax (macros)**: Min/max comparison utilities

## Dependencies
- Platform-specific macros for calling conventions (GCALL)
- Compiler-specific pragmas for warning suppression
- Watcom-specific inline assembly for memory operations
