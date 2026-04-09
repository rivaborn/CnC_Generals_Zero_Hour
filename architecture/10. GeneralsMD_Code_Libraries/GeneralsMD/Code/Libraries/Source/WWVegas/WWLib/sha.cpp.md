# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/sha.cpp

## Purpose
Implements the SHA-1 cryptographic hash algorithm for data integrity verification.

## Responsibilities
- Processes arbitrary-length data blocks into a 20-byte hash digest
- Manages partial block buffering for incremental hashing
- Performs core SHA-1 transformations on 512-bit blocks
- Provides utility functions for bit rotation and byte reversal

## Key Types
- `SHAEngine` (Class): Main SHA-1 processing engine
- `SHADigest` (Struct): Contains the 5 intermediate hash values (20 bytes total)
- `Partial` (Buffer): Temporary storage for partial data blocks

## Key Functions
### `SHAEngine::Hash`
- Purpose: Processes input data and updates the hash state
- Calls: `Process_Partial`, `Process_Block`

### `SHAEngine::Process_Block`
- Purpose: Applies SHA-1 transformation to a 512-bit block
- Calls: `_rotl`, `Do_Function`, `Get_Constant`

### `_rotl`
- Purpose: Performs circular bit rotation on integer values
- Calls: None (template function)

### `memrev`
- Purpose: Reverses byte order in a buffer
- Calls: None

## Globals
- `IsCached` (bool): Tracks if final result is precomputed
- `Length` (long): Total bytes processed
- `PartialCount` (int): Bytes in partial buffer
- `Acc` (SHADigest): Current hash accumulator state

## Dependencies
- `sha.h`: Header with SHA-1 definitions
- `<iostream.h>`: Standard I/O
- `<stdlib.h>`: Memory functions
- `memcpy`, `memset`: Memory operations
