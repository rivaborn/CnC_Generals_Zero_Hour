# GeneralsMD/Code/Libraries/Source/Compression/EAC/btreeabout.cpp

## Purpose
Provides metadata about the BTree compression codec via the `BTREE_about` function.

## Responsibilities
- Allocates and initializes a `CODEXABOUT` structure.
- Sets codec identification fields (signature, version, type).
- Indicates supported operations (decode/encode, 32-bit size).

## Key Types
- `CODEXABOUT` (struct): Holds codec metadata (signature, version, capabilities).

## Key Functions
### BTREE_about
- Purpose: Returns a `CODEXABOUT` struct describing the BTree codec.
- Calls: `galloc`, `memset`, `strcpy`.

## Globals
- None.

## Dependencies
- `string.h` (for `memset`, `strcpy`).
- `codex.h` (for `CODEXABOUT`).
- `btreecodex.h` (not shown in snippet, but referenced in comments).
- `galloc` (memory allocation function).
