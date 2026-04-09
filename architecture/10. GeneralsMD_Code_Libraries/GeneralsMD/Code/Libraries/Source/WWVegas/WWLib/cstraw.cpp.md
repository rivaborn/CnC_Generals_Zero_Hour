# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/cstraw.cpp

## Purpose
Implements the `CacheStraw::Get` method for fetching data from a data source with buffering to optimize small requests.

## Responsibilities
- Buffers data to reduce multiple small read operations
- Manages internal buffer state (index, length)
- Delegates to underlying `Straw` for actual data retrieval
- Handles partial reads and end-of-data conditions

## Key Types
- `CacheStraw` (Class): Buffered data access wrapper
- `Straw` (Class): Base data source interface (external)

## Key Functions
### `CacheStraw::Get`
- Purpose: Fetches requested data with internal buffering to optimize performance
- Calls: `Straw::Get`, `memmove`

## Globals
- None

## Dependencies
- `always.h`, `cstraw.h`, `string.h`
- `Straw` class methods
- `memmove` from C runtime
