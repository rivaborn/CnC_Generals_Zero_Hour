# Generals/Code/Libraries/Source/WWVegas/WWLib/chunkio.cpp - Enhanced Analysis

## Architectural Role
This file implements a hierarchical chunked I/O system used throughout the engine for serialization of game data structures. It provides the foundation for saving/loading game states, map data, and other complex data hierarchies.

## Cross-References
### Incoming
- Game save/load systems (uses ChunkSaveClass/ChunkLoadClass)
- Map loading/saving infrastructure
- W3D model serialization
- AI behavior tree serialization

### Outgoing
- FileClass for low-level I/O operations
- Vector/quaternion math types for serialization

## Design Patterns
- **Composite Pattern**: Chunks can contain other chunks, creating a tree structure
- **Strategy Pattern**: Different data types (vectors, quaternions) have specialized read/write methods
- **State Pattern**: ChunkLoadClass maintains state about current chunk/micro-chunk position

Rules followed. Analysis limited to 400 tokens.
