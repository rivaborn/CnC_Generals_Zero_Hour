# GeneralsMD/Code/Libraries/Source/Compression/EAC/btreedecode.cpp

## Purpose
Implements B-tree decompression for the EAC compression library, used for decoding compressed data in the game.

## Responsibilities
- Decompresses data using B-tree algorithm
- Validates compressed data format
- Determines uncompressed data size
- Provides interface for decoding operations

## Key Types
- BTreeDecodeContext (Class): Holds decompression state (clue table, node pointers, output buffer)

## Key Functions
### BTREE_chase
- Purpose: Recursively traverses B-tree nodes to output leaf values
- Calls: BTREE_chase (recursive)

### BTREE_decompress
- Purpose: Main decompression function that processes compressed data
- Calls: BTREE_chase, ggetm

### BTREE_is
- Purpose: Checks if data has valid B-tree compression header
- Calls: ggetm

### BTREE_size
- Purpose: Returns uncompressed data size from compressed header
- Calls: ggetm

### BTREE_decode
- Purpose: Public interface for decompression
- Calls: BTREE_decompress

## Globals
- None

## Dependencies
- codex.h (ggetm)
- btreecodex.h
- string.h
