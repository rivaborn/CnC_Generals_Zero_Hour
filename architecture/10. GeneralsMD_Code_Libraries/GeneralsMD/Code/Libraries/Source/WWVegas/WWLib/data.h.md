# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/data.h

## Purpose
Declares functions for loading and fetching game resources like images, strings, and compressed data.

## Responsibilities
- Define resource loading functions
- Declare string and resource fetching APIs
- Include necessary headers for file and buffer operations

## Key Types
None

## Key Functions
### Load_Picture
- Purpose: Loads a picture from a file into a buffer with optional palette.
- Calls: Not inferable

### Load_Alloc_Data
- Purpose: Allocates and loads data from a file.
- Calls: Not inferable

### Load_Uncompress
- Purpose: Decompresses data from a file into a destination buffer.
- Calls: Not inferable

### Fetch_String
- Purpose: Retrieves a string by its ID.
- Calls: Not inferable

### Fetch_Resource
- Purpose: Fetches a resource by name and type.
- Calls: Not inferable

## Globals
None

## Dependencies
- `buff.h`: Buffer operations
- `iff.h`: IFF file format handling
- `win.h`: Windows API headers
- `wwfile.h`: Westwood file I/O utilities
- `TXT_NONE`: Constant for no text (value 0)
