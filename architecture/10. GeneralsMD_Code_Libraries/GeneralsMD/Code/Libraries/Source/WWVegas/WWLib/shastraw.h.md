# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/shastraw.h

## Purpose
This file defines a `SHAStraw` class that generates a Secure Hash Algorithm (SHA) hash from data flowing through it without modifying the data stream.

## Responsibilities
- Inherits from `Straw` to process data streams.
- Computes SHA hashes of the data stream.
- Provides methods to enable/disable hash computation.
- Retrieves the resulting hash value.

## Key Types
- **SHAStraw (Class)**: A straw (data stream processor) that computes SHA hashes of the data it processes.

## Key Functions
### SHAStraw::Get
- Purpose: Processes data and updates the SHA hash.
- Calls: Not inferable (implementation in .cpp file).

### SHAStraw::Result
- Purpose: Retrieves the computed SHA hash result.
- Calls: Not inferable.

### SHAStraw::Disable
- Purpose: Disables hash computation.
- Calls: None.

### SHAStraw::Enable
- Purpose: Enables hash computation.
- Calls: None.

## Globals
- None.

## Dependencies
- `sha.h`: SHA hash engine definitions.
- `straw.h`: Base `Straw` class definition.
- `SHAEngine`: Used internally for hash computation.
