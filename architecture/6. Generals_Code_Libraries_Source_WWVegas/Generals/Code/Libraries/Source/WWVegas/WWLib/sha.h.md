# Generals/Code/Libraries/Source/WWVegas/WWLib/sha.h

## Purpose
Implements the Secure Hash Algorithm (SHA-1) for cryptographic hashing.

## Responsibilities
- Provides SHA-1 hashing functionality
- Manages block processing and partial data handling
- Caches final hash results for efficiency
- Exposes hash size and constant values

## Key Types
- **SHAEngine (Class)**: Main SHA-1 hashing engine
- **SHADigest (Class)**: Union for 20-byte hash storage (5 longs or 20 chars)
- **Anonymous enum**: Contains SHA constants (SA, SB, SC, SD, SE, K1-K4, block sizes)

## Key Functions
### SHAEngine::Result
- Purpose: Retrieves the final hash result
- Calls: Not inferable (implementation in .cpp)

### SHAEngine::Hash
- Purpose: Processes input data and updates hash state
- Calls: Process_Partial, Process_Block

### SHAEngine::Process_Block
- Purpose: Processes a full 512-bit source data block
- Calls: Do_Function, Get_Constant

### SHAEngine::Process_Partial
- Purpose: Handles partial source data blocks
- Calls: Not inferable

### SHAEngine::Do_Function
- Purpose: Selects appropriate SHA function based on index
- Calls: Function1-4

## Globals
- **SHA_SOURCE1/2/3 (String)**: Test vectors for SHA-1
- **SHA_DIGEST1a/b/2a/b/3a/b (Byte arrays)**: Expected hash results for test vectors

## Dependencies
- `<new.h>`, `<stdio.h>`, `<stdlib.h>`, `<string.h>`
- `bool.h`, `always.h` (custom headers)
- Uses placement new for
