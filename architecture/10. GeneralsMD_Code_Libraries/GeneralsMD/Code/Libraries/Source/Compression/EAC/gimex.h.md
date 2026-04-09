# GeneralsMD/Code/Libraries/Source/Compression/EAC/gimex.h

## Purpose
Header file defining the GIMEX API for graphics import/export operations.

## Responsibilities
- Declares data structures for image metadata and file handling
- Defines function prototypes for image I/O operations
- Provides cross-platform memory access utilities
- Specifies version and compatibility information

## Key Types
- **ARGB (struct)**: Color channel structure (b,g,r,a or platform-specific order)
- **GINFO (struct)**: Image metadata (dimensions, palette, hotspots, etc.)
- **GINSTANCE (struct)**: File handle and frame management
- **GABOUT (struct)**: Format capabilities and limitations
- **GBITMAP (struct)**: Bitmap data container
- **GFUNCTIONS (struct)**: Function pointer table for GIMEX implementation

## Key Functions
### GIMEX_open
- Purpose: Opens an image file for reading
- Calls: Not visible in header

### GIMEX_read
- Purpose: Reads image data into a buffer
- Calls: Not visible in header

### GIMEX_write
- Purpose: Writes image data from a buffer
- Calls: Not visible in header

### ggetm/ggeti
- Purpose: Cross-platform memory access (Motorola/Intel byte order)
- Calls: None

### gputm/gputi
- Purpose: Cross-platform memory writing (Motorola/Intel byte order)
- Calls: None

## Globals
- **gfunctions (GFUNCTIONS[])**: Array of function pointers for GIMEX implementation

## Dependencies
- `<stdlib.h>` for `malloc`/`free`
- Platform-specific types (`__int64`, `long`, `long long`)
- Compiler-specific pragmas (`_MSC_VER`, `__R5900`, etc.)
