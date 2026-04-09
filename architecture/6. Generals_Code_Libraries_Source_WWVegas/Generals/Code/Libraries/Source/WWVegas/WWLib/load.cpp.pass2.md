# Generals/Code/Libraries/Source/WWVegas/WWLib/load.cpp - Enhanced Analysis

## Architectural Role
This file is part of the core asset loading pipeline in the SAGE engine, specifically handling decompression of game assets. It bridges the low-level file I/O layer with the higher-level resource management systems, ensuring compressed assets are properly decompressed before use in rendering, audio, or game logic.

## Cross-References
### Incoming
- `WWSaveLoad/saveload.cpp` (calls `Uncompress_Data` for save/load operations)
- `WWDownload/Download.cpp` (likely uses decompression for downloaded content)

### Outgoing
- `lcw.h` (for LCW compression/decompression)
- Platform-specific byte-order functions (`Reverse_Long`, `Reverse_Word`)

## Design Patterns
- **Strategy Pattern**: Compression method selection via `switch` on `CompressionType`.
- **Facade Pattern**: Hides compression details behind `Uncompress_Data` API.
- **Not inferable**: No clear use of other patterns (e.g., no factories, observers).

*(Token count: ~200)*
