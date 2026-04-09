# Generals/Code/Libraries/Source/WWVegas/WWLib/lcw.cpp - Enhanced Analysis

## Architectural Role
This file implements the core LCW compression/decompression algorithm used throughout the SAGE engine for asset data (e.g., W3D models, textures). It's a low-level utility library that other subsystems depend on for efficient data storage/loading.

## Cross-References
### Incoming
- Likely called by asset loading systems (e.g., W3D model loader, texture manager)
- Possibly used by save/load game functionality for compressed data chunks

### Outgoing
- None (standalone utility with no external dependencies)

## Design Patterns
- **Command Pattern**: Decompression uses op-codes as commands (e.g., 0x80 for end-of-data)
- **Inline Assembly Optimization**: Compression uses platform-specific assembly for performance
- **State Machine**: Decompression processes op-codes in a loop with conditional branches

*Not inferable*: No clear use of other patterns (e.g., no factories, decorators, or observers visible).
