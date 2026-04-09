# GeneralsMD/Code/Libraries/Source/Compression/EAC/btreecodex.h

## Purpose
Header file for B-tree based compression/decompression functions in the EAC codec library.

## Responsibilities
- Declares B-tree codec API functions for compression/decompression
- Provides information queries about compressed data
- Exposes C-compatible interface with C++ overloads

## Key Types
- CODEXABOUT (Type): Not inferable (external type)
- None (other types)

## Key Functions
### BTREE_about
- Purpose: Returns codec information
- Calls: None

### BTREE_is
- Purpose: Checks if data is B-tree compressed
- Calls: None

### BTREE_size
- Purpose: Returns decompressed size from compressed data
- Calls: None

### BTREE_decode
- Purpose: Decompresses B-tree compressed data
- Calls: None

### BTREE_encode
- Purpose: Compresses data using B-tree algorithm
- Calls: None

## Globals
- None

## Dependencies
- codex.h (required include)
- CODEXABOUT (external type)
- GCALL (macro for calling convention)
