# GeneralsMD/Code/Libraries/Source/Compression/EAC/refcodex.h

## Purpose
Header file defining the REF (Reference) compression codec API for data compression/decompression.

## Responsibilities
- Declares REF codec function prototypes for compression/decompression
- Provides metadata query functions for compressed data
- Defines internal utility macros (qmin, qmax)
- Enforces proper include order (codex.h must be included first)

## Key Types
- CODEXABOUT (Struct): Contains codec metadata/version information
- None (other types are opaque pointers)

## Key Functions
### REF_about
- Purpose: Returns codec metadata/version information
- Calls: None

### REF_is
- Purpose: Checks if data is valid REF-compressed data
- Calls: None

### REF_size
- Purpose: Returns decompressed size of REF-compressed data
- Calls: None

### REF_decode
- Purpose: Decompresses REF-compressed data into destination buffer
- Calls: None

### REF_encode
- Purpose: Compresses source data into REF-compressed format
- Calls: None

## Globals
- None

## Dependencies
- codex.h (required include)
- GCALL macro (calling convention)
- bool type (C++ compatibility)
