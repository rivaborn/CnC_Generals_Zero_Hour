# Generals/Code/Libraries/Source/WWVegas/WWLib/data.cpp

## Purpose
Handles file loading, resource fetching, and string management for the game engine.

## Responsibilities
- Load and allocate file data into memory
- Decompress compressed data from files
- Fetch string and resource data from the executable
- Manage high-resolution file loading

## Key Types
- **SRecord (Class)**: Tracks string resource ID, timestamp, and content for caching
- **CompHeaderType (Struct)**: Not inferable (used in Load_Uncompress)

## Key Functions
### Load_Alloc_Data
- Purpose: Allocates memory and loads file contents
- Calls: `W3DNEWARRAY`, `file.Read()`

### Load_Uncompress
- Purpose: Loads and decompresses data from a file
- Calls: `file.Read()`, `file.Seek()`, `Uncompress_Data()`

### Fetch_String
- Purpose: Retrieves string resources with caching
- Calls: `LoadString()`

### Fetch_Resource
- Purpose: Loads embedded resources from the executable
- Calls: `FindResource()`, `LoadResource()`, `LockResource()`

### Hires_Load
- Purpose: Loads resolution-dependent files
- Calls: `W3DNEWARRAY`, `file.Read()`

## Globals
- **_buffers (SRecord[64])**: String resource cache
- **_time (int)**: Timestamp counter for cache management

## Dependencies
- `always.h`, `data.h`
- `FileClass`, `Buffer` classes
- `Uncompress_Data()` function
- Windows API (`FindResource`, `LoadResource`, etc.)
