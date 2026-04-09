# GeneralsMD/Code/Libraries/Source/Compression/EAC/btreeencode.cpp

## Purpose
Implements a B-tree based compression algorithm for the game engine.

## Responsibilities
- Compresses data using a B-tree encoding scheme
- Manages bit-level writing and buffer handling
- Handles frequency counting and node joining for compression
- Supports zero suppression for ASCII data

## Key Types
- **BTREEMemStruct (struct)**: Tracks pointer and length for memory buffers
- **BTreeEncodeContext (struct)**: Main compression context with bit packing state and buffers
- **None**: No classes/enums defined

## Key Functions
### BTREE_writebits
- Purpose: Writes a bit pattern to the output buffer
- Calls: Recursively calls itself for patterns >16 bits

### BTREE_adjcount
- Purpose: Counts adjacent byte pairs in the input buffer
- Calls: None (uses macros for counting)

### BTREE_joinnodes
- Purpose: Joins nodes in the compression tree
- Calls: None

### BTREE_findbest
- Purpose: Finds the 48 most common nodes for compression
- Calls: None

### BTREE_treepack
- Purpose: Main compression routine that builds the B-tree
- Calls: BTREE_writebits, BTREE_adjcount, BTREE_clearcount, BTREE_joinnodes, BTREE_findbest

### BTREE_compressfile
- Purpose: Compresses a file using B-tree encoding
- Calls: BTREE_treepack, BTREE_writebits

### BTREE_encode
- Purpose: Public interface for compression
- Calls: BTREE_compressfile

## Globals
- **None**: All variables are local or static

## Dependencies
- Key includes: "codex.h", "btreecodex.h"
- External symbols: galloc, gfree (memory allocation), memcpy
- Uses BTREECODES (256), BTREEBIGNUM (32000), BTREESLOPAGE (16384) constants
