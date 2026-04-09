# Generals/Code/Tools/WW3D/pluglib/chunkio.cpp - Enhanced Analysis

## Architectural Role
This file implements the core chunked I/O system for W3D assets, enabling hierarchical serialization of game data. It bridges the low-level FileClass interface with higher-level asset loading/saving systems, particularly for 3D models and animations.

## Cross-References
### Incoming
- Asset loading pipeline (e.g., W3D model loaders)
- Animation system (for keyframe data serialization)
- Modding tools (custom asset creation/export)

### Outgoing
- FileClass (raw file I/O operations)
- Math library (vector/quaternion serialization)

## Design Patterns
- **State Pattern**: ChunkLoadClass maintains internal state (chunk depth, micro-chunk status) to control reading behavior
- **Composite Pattern**: Nested chunk hierarchy allows complex data structures to be serialized recursively
- **Template Method**: Overloaded Read/Write methods for different data types follow a consistent interface pattern

Rules followed. Analysis limited to observable code characteristics.
