# GeneralsMD/Code/Libraries/Source/Compression/EAC/codex.h

## Purpose
Defines the CODEX compression/decompression API for Generals Zero Hour.

## Responsibilities
- Declares CODEXABOUT structure for module metadata
- Defines QFUNCTIONS struct for compression/decompression function pointers
- Provides function prototypes for CODEX operations
- Establishes version and calling convention macros

## Key Types
- CODEXABOUT (struct): Contains metadata about a CODEX module (version, capabilities, strings)
- QFUNCTIONS (struct): Holds function pointers for CODEX operations (about, is, size, decode, encode)

## Key Functions
### CODEX_about
- Purpose: Returns module information via CODEXABOUT structure
- Calls: None

### CODEX_is
- Purpose: Checks if data is in CODEX compressed format
- Calls: None

### CODEX_size
- Purpose: Returns decompressed size of CODEX data
- Calls: None

### CODEX_decode
- Purpose: Decompresses CODEX data into destination buffer
- Calls: None

### CODEX_encode
- Purpose: Compresses data into CODEX format
- Calls: None

## Globals
- qfunctions (QFUNCTIONS[]): Array of QFUNCTIONS structs for different CODEX modules

## Dependencies
- gimex.h (for memory IO)
- Uses GCALL macro (defined in this file) for calling convention
- QMAKEID macro for creating 32-bit IDs
