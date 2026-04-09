# GeneralsMD/Code/GameEngine/Source/Common/System/ArchiveFile.cpp - Enhanced Analysis

## Architectural Role
This file implements the core virtual filesystem abstraction for archived content, bridging between the physical file system (via `File`) and higher-level subsystems like W3D (for asset loading) and modding infrastructure. It enables path-based file discovery and metadata retrieval without direct OS file access.

## Cross-References
### Incoming
- `StreamingArchiveFile.cpp` (uses `ArchiveFile` for metadata lookup)
- Likely called by W3D asset loaders and modding tools for file discovery

### Outgoing
- Directly uses `File` for low-level I/O operations
- Relies on `AsciiString` for path manipulation and wildcard matching

## Design Patterns
- **Composite Pattern**: Hierarchical directory structure using `DetailedArchivedDirectoryInfo` nodes
- **Visitor-like traversal**: Recursive directory walking in `getFileListInDirectory`
- **Strategy Pattern**: Wildcard matching as a reusable string comparison strategy

*Not inferable*: No clear use of Factory, Observer, or other patterns in this file alone.
