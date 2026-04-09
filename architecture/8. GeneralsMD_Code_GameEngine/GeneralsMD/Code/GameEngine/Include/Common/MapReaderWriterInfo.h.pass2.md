# GeneralsMD/Code/GameEngine/Include/Common/MapReaderWriterInfo.h - Enhanced Analysis

## Architectural Role
This header defines the core I/O abstraction layer for map file handling in the SAGE engine, bridging the game's map data structures with file system operations. It enables versioned map serialization/deserialization, critical for modding support and cross-version compatibility.

## Cross-References
### Incoming
- Map loading/saving systems (e.g., `MapReader`, `MapWriter`)
- Modding tools that need to read/write map files
- Terrain editing components using height/blend tile versions

### Outgoing
- File system abstractions (commented `FileInputStream` suggests original file-based implementation)
- Compression systems (cached buffer enables transparent compression)
- Memory management for buffered I/O

## Design Patterns
- **Bridge Pattern**: Abstracts I/O operations from concrete file/stream implementations
- **Versioning Strategy**: Uses constant-based versioning for backward compatibility
- **Template Method**: Virtual stream interfaces enforce read/write contracts while allowing custom implementations

*Not inferable*: Exact compression mechanism or error handling strategy.
