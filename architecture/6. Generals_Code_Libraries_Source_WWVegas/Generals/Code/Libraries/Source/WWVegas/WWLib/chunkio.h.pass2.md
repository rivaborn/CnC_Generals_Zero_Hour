# Generals/Code/Libraries/Source/WWVegas/WWLib/chunkio.h - Enhanced Analysis

## Architectural Role
This file defines the core chunk-based file I/O system used throughout the SAGE engine for serialization of game assets (W3D models, animations) and save games. The chunk format enables hierarchical data organization with forward/backward compatibility via micro-chunks.

## Cross-References
### Incoming
- W3D model loading pipeline (W3DLoader)
- Save/load game systems
- Asset serialization for all game objects
- Modding infrastructure (custom asset loading)

### Outgoing
- FileClass (WWLib) for low-level I/O
- Memory allocation (via WWLib utilities)
- String handling (WWString/WideString)

## Design Patterns
- **Composite Pattern**: Chunks can contain other chunks recursively (depth-limited to 256)
- **Adapter Pattern**: Micro-chunks adapt simple variables into chunk format without full overhead
- **Template Method**: Macros like WRITE_WWSTRING_CHUNK abstract common serialization patterns

*Not inferable*: Exact error handling strategy for corrupted chunks.
