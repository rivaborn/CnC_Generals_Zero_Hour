# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/chunkio.cpp - Enhanced Analysis

## Architectural Role
This file implements a hierarchical chunked I/O system that underpins the engine's serialization infrastructure. It enables structured file formats for game assets (W3D models, mission data) and save games, with support for nested data organization and versioning.

## Cross-References
### Incoming
- W3D model loader (uses chunked format for mesh/animation data)
- Save game system (serializes game state hierarchically)
- Mission file parser (handles scenario data chunks)

### Outgoing
- FileClass (low-level file operations)
- Math library types (IOVector2/3/4Struct, IOQuaternionStruct)

## Design Patterns
- **Composite Pattern**: Chunks can contain other chunks, enabling recursive data organization
- **Strategy Pattern**: Different data types (vectors, quaternions) use specialized read/write methods
- **State Pattern**: ChunkLoadClass tracks current chunk state (depth, position) during parsing

Rules followed. Output under 400 tokens.
