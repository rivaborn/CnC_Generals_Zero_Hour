# Generals/Code/Libraries/Source/WWVegas/WWLib/data.h

## Purpose
Header file declaring functions for loading and fetching game resources like images, strings, and compressed data.

## Responsibilities
- Declares resource loading functions
- Defines buffer and file manipulation utilities
- Provides string and resource fetching interfaces
- Includes necessary headers for data handling

## Key Types
None

## Key Functions
### Load_Picture
- Purpose: Loads an image from a file into a buffer with optional palette conversion
- Calls: Not inferable

### Load_Alloc_Data
- Purpose: Allocates and loads data from a file
- Calls: Not inferable

### Load_Uncompress
- Purpose: Decompresses data from a file into a destination buffer
- Calls: Not inferable

### Fetch_String
- Purpose: Retrieves a localized string by ID
- Calls: Not inferable

### Fetch_Resource
- Purpose: Fetches a resource by name and type
- Calls: Not inferable

## Globals
- TXT_NONE (int): Constant for no text

## Dependencies
- buff.h: Buffer manipulation
- iff.h: IFF file format handling
- win.h: Windows-specific types
- wwfile.h: File I/O utilities
