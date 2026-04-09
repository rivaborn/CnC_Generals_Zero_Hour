# GeneralsMD/Code/Libraries/Source/Compression/EAC/huffdecode.cpp - Enhanced Analysis

## Architectural Role
This file implements the core Huffman decompression logic for the game's asset pipeline, serving as the inverse of the compression system. It's part of the EAC (Electronic Arts Compression) library, which handles data compression/decompression for game assets like textures, models, and audio.

## Cross-References
### Incoming
- Likely called by asset loading systems (e.g., W3D model loader, texture manager) when decompressing embedded data
- May be invoked by the modding infrastructure when loading user-created content

### Outgoing
- Uses `ggetm` from `codex.h` for memory reads (endianness handling)
- Relies on `GCALL` calling convention macro for cross-platform compatibility

## Design Patterns
- **Bit Manipulation State Machine**: The decompression uses a stateful bit buffer (`bits`, `bitsleft`) with macros like `SQgetbits` to efficiently extract variable-length codes
- **Strategy Pattern (Implicit)**: Different decompression strategies for delta/accelerated modes are handled via conditional logic
- **Macro-Based Optimization**: Performance-critical operations (bit extraction, memset) are implemented as macros to reduce function call overhead
