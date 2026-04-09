# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/lzo.h - Enhanced Analysis

## Architectural Role
This header provides the compression/decompression infrastructure for the SAGE engine, critical for asset loading and network serialization. The LZOCompressor wrapper abstracts low-level LZO operations, enabling consistent buffer management across subsystems.

## Cross-References
### Incoming
- Asset loading pipeline (e.g., W3D model loading)
- Network serialization for multiplayer
- Save/load system

### Outgoing
- External LZO implementation (lzo1x.h)
- Memory allocation subsystem (via work buffer)

## Design Patterns
- **Facade Pattern**: LZOCompressor hides LZO implementation details
- **Static Wrapper**: Encapsulates work buffer management
- **Buffer Pooling**: Pre-allocated work buffer avoids runtime allocation overhead

*Not inferable*: No other patterns evident from header alone.
