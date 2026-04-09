# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/load.cpp - Enhanced Analysis

## Architectural Role
This file is part of the low-level I/O and compression subsystem, providing core functionality for loading and decompressing game assets. It bridges the file system layer with the asset loading pipeline, handling compressed data formats used throughout the engine.

## Cross-References
### Incoming
- `Uncompress_Data` is called by `SaveLoadSystemClass::Load` (saveload.cpp) for handling compressed save game data
- Likely used by asset loading systems (e.g., W3D model loading) though not explicitly cross-referenced

### Outgoing
- Calls `LCW_Uncomp` from lcw.h for LCW compression format
- Uses `memmove` for uncompressed data handling
- Conditionally uses `Reverse_Long`/`Reverse_Word` for Amiga byte-order conversion

## Design Patterns
- **Strategy Pattern**: Different compression methods (NOCOMPRESS, LCW) are handled via conditional dispatch
- **Facade Pattern**: Provides a unified interface for decompression despite multiple underlying formats
- **Data-Driven Design**: Compression method determined at runtime from header metadata

*Not inferable*: Exact callers beyond save/load system remain unclear from cross-references.
