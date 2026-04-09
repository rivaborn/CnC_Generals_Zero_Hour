# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/lzopipe.cpp - Enhanced Analysis

## Architectural Role
This file implements the LZO compression/decompression pipeline, serving as a critical component in the SAGE engine's data processing infrastructure. It handles block-based compression/decompression and integrates with the pipe system for data flow management, particularly important for asset loading and network operations.

## Cross-References
### Incoming
- **Asset Loading System**: Likely called during map/asset decompression
- **Network Layer**: Used for compressing/decompressing network packets
- **Save/Load System**: May be used for compressing save game data

### Outgoing
- **LZO Library**: Directly calls `lzo1x_decompress` and `lzo1x_1_compress`
- **Pipe System**: Inherits from and calls `Pipe::Put` and `Pipe::Flush`
- **Memory Management**: Uses `new`/`delete` for buffer allocation

## Design Patterns
- **Pipeline Pattern**: Implements a processing pipeline for data compression/decompression
- **Buffer Accumulation**: Uses internal buffers to accumulate data before processing blocks
- **Strategy Pattern**: `CompControl` enum selects between compression/decompression strategies

*Not inferable*: Exact callers of this class in the engine hierarchy.
