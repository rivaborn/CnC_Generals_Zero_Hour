# GeneralsMD/Code/Libraries/Source/Compression/EAC/refabout.cpp

## Purpose
Provides metadata about the REF (RefPack) compression codec via the `REF_about` function.

## Responsibilities
- Exposes codec capabilities (decode/encode support, 32-bit size field).
- Returns version and type strings for the REF codec.
- Allocates and initializes a `CODEXABOUT` structure with codec info.

## Key Types
- `CODEXABOUT` (struct): Holds codec metadata (signature, version, capabilities, strings).

## Key Functions
### `REF_about`
- Purpose: Returns a `CODEXABOUT` struct describing the REF codec.
- Calls: `galloc`, `memset`, `strcpy`.

## Globals
- None.

## Dependencies
- `string.h` (for `memset`, `strcpy`).
- `codex.h` (for `CODEXABOUT`, `QMAKEID`, `galloc`).
- `refcodex.h` (header for REF codec).
