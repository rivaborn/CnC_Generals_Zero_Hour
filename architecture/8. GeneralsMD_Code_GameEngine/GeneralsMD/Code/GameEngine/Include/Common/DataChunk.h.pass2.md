# GeneralsMD/Code/GameEngine/Include/Common/DataChunk.h - Enhanced Analysis

## Architectural Role
This file defines the core chunked file I/O system used throughout the engine for serialization of game data, including save games, maps, and mod assets. It provides versioned, hierarchical chunking with parser registration, forming the foundation for the engine's data persistence layer.

## Cross-References
### Incoming
- **Save/Load System**: Uses `DataChunkInput`/`DataChunkOutput` for game state serialization
- **Map System**: Relies on chunked format for map data (via `MapReaderWriterInfo.h`)
- **Modding Infrastructure**: Custom parsers registered for mod-specific data chunks
- **W3D Model System**: Likely uses chunks for model asset serialization

### Outgoing
- **Memory Management**: Uses `MemoryPoolObject` and `GameMemory.h` for object allocation
- **Stream Abstractions**: Depends on `OutputStream`/`ChunkInputStream` for I/O
- **Dictionary System**: Uses `Dict.h` for structured data serialization

## Design Patterns
- **Strategy Pattern**: Parser registration allows dynamic handling of different chunk types
- **Composite Pattern**: Chunk hierarchy (parent/child relationships) for structured data
- **Flyweight Pattern**: `DataChunkTableOfContents` caches name-ID mappings to avoid duplication

*Not inferable*: Exact implementation details of parser dispatch or chunk traversal.
