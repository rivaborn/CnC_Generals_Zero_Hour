# GeneralsMD/Code/Libraries/Source/Compression/EAC/huffabout.cpp

## Purpose
Provides metadata about the Huffman compression codec via the `HUFF_about` function.

## Responsibilities
- Exposes codec capabilities (encoding/decoding support, version info).
- Returns a `CODEXABOUT` structure with codec details.
- Allocates and initializes the info structure.

## Key Types
- `CODEXABOUT` (struct): Contains codec metadata (signature, version, capabilities).

## Key Functions
### `HUFF_about`
- Purpose: Returns a `CODEXABOUT` structure describing the Huffman codec.
- Calls: `galloc`, `memset`, `strcpy`.

## Globals
- None.

## Dependencies
- `string.h` (for `memset`, `strcpy`).
- `codex.h` (for `CODEXABOUT`).
- `huffcodex.h` (not shown in snippet, likely for codec-specific types).
- `galloc` (memory allocation function).
