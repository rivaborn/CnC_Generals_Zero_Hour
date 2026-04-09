# Generals/Code/Libraries/Source/WWVegas/WWLib/rle.cpp - Enhanced Analysis

## Architectural Role
This file implements core RLE compression/decompression utilities used throughout the engine for optimizing texture and sprite data storage. The RLEEngine class provides low-level byte manipulation services consumed by higher-level rendering and asset systems.

## Cross-References
### Incoming
- Likely called by texture/sprite loading systems (e.g., W3D asset pipeline)
- Potentially used by network serialization for efficient data transfer
- May be referenced by UI systems for compressed bitmap storage

### Outgoing
- Directly manipulates memory buffers (no external subsystem calls)
- Relies on "always.h" for MIN macro and basic utilities

## Design Patterns
- **Utility Class**: RLEEngine encapsulates standalone compression/decompression algorithms
- **Data Transformation**: Pure transformation pattern with no side effects
- **Null Object**: Handles NULL destination buffers for length calculation

*Not inferable*: No clear strategy/observer patterns visible in this isolated utility.
