# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/data.cpp

## Purpose
Handles file loading, resource fetching, and data decompression for the game engine.

## Responsibilities
- Load and allocate file data into memory
- Decompress compressed data from files
- Fetch string and resource data
- Manage high-resolution file loading

## Key Types
- **SRecord (Class)**: Stores string resource data (ID, timestamp, string content)
- **CompHeaderType (Not inferable)**: Used in decompression (defined elsewhere)

## Key Functions
### Load_Alloc_Data
- Purpose: Allocates memory and loads file contents
- Calls: `file.Is_Available()`, `file.Size()`, `file.Read()`

### Load_Uncompress
- Purpose: Loads and decompresses data from a file
- Calls: `file.Is_Open()`, `file.Open()`, `file.Read()`, `file.Seek()`, `Uncompress_Data()`

### Fetch_String
- Purpose: Retrieves string resources with caching
- Calls: `LoadString()`

### Fetch_Resource
- Purpose: Fetches Windows resources by name/type
- Calls: `FindResource()`, `LoadResource()`, `LockResource()`

### Hires_Load
- Purpose: Loads resolution-dependent files
- Calls: `file.Is_Available()`, `file.Size()`, `file.Read()`

## Globals
- **_buffers (SRecord[64])**: Caches fetched strings
- **_time (int)**: Tracks string request timestamps

## Dependencies
- `always.h`, `data.h`
- `FileClass`, `Buffer` classes
- Windows API (`HRSRC`, `HGLOBAL`, etc.)
- `Uncompress_Data()` (external)
- `LoadString()` (Windows API)
