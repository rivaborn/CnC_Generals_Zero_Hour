# GeneralsMD/Code/Libraries/Source/Compression/EAC/refdecode.cpp

## Purpose
Implements reference decoding for EAC (Electronic Arts Compression) format, handling header validation, size extraction, and decompression.

## Responsibilities
- Validate compressed data headers
- Extract uncompressed size from compressed data
- Decompress EAC-compressed data into destination buffer

## Key Types
None

## Key Functions
### REF_is
- Purpose: Check if data is valid EAC-compressed format
- Calls: ggetm

### REF_size
- Purpose: Extract uncompressed size from EAC-compressed data
- Calls: ggetm

### REF_decode
- Purpose: Decompress EAC-compressed data into destination buffer
- Calls: None (uses direct pointer arithmetic)

## Globals
None

## Dependencies
- `codex.h`, `refcodex.h` (for ggetm function)
- External: `ggetm` (multi-byte get function)
