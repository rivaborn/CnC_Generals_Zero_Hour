# Generals/Code/Libraries/Source/WWVegas/WWLib/sha.cpp

## Purpose
Implements the SHA-1 cryptographic hash algorithm for data integrity verification.

## Responsibilities
- Processes arbitrary-length data blocks into a 20-byte hash digest
- Manages partial block buffering and full block processing
- Performs bitwise rotations and byte reversals for SHA-1 operations
- Maintains hash state across multiple data chunks

## Key Types
- `SHAEngine` (Class): Main SHA-1 processing engine
- `SHADigest` (Struct): Contains 5 32-bit words representing hash state
- `_rotl` (Template function): Performs circular bit rotation

## Key Functions
### `SHAEngine::Hash`
- Purpose: Processes input data and updates hash state
- Calls: `Process_Partial`, `Process_Block`

### `SHAEngine::Process_Block`
- Purpose: Processes a full 512-bit block into the hash accumulator
- Calls: `_rotl`, `Do_Function`, `Get_Constant`

### `SHAEngine::Result`
- Purpose: Computes final hash digest and returns it
- Calls: `Process_Block`, `memcpy`

## Globals
- `Reverse_LONG` (Macro): Reverses byte order of 32-bit value

## Dependencies
- `sha.h` (header)
- `<iostream.h>`
- `<stdlib.h>`
- `memcpy`, `memset` (standard library functions)
