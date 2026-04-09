# Generals/Code/Libraries/Source/WWVegas/WWLib/shastraw.h

## Purpose
Defines a `SHAStraw` class that computes a Secure Hash Algorithm (SHA) hash from data flowing through it without modifying the data stream.

## Responsibilities
- Inherits from `Straw` to process data streams.
- Computes SHA hash incrementally as data passes through.
- Provides methods to enable/disable hashing.
- Exposes the final hash result.

## Key Types
- **SHAStraw (Class)**: A straw (data stream processor) that computes SHA hashes.

## Key Functions
### SHAStraw::Get
- Purpose: Processes data and updates the SHA hash incrementally.
- Calls: `SHAEngine` methods (not visible in header).

### SHAStraw::Result
- Purpose: Retrieves the computed SHA hash result.
- Calls: None (header-only).

### SHAStraw::Disable / Enable
- Purpose: Toggles hashing on/off without modifying the data stream.
- Calls: None.

## Globals
- None.

## Dependencies
- `sha.h` (SHAEngine class).
- `straw.h` (Straw base class).
