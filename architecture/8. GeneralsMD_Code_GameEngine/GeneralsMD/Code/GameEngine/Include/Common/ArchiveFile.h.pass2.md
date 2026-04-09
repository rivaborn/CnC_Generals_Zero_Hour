# GeneralsMD/Code/GameEngine/Include/Common/ArchiveFile.h - Enhanced Analysis

## Architectural Role
This file defines the abstract base class for archive file handling in the SAGE engine's resource management system. It serves as the interface for accessing files stored within archive files (e.g., mix files), enabling the engine to treat archives as virtual file systems.

## Cross-References
### Incoming
- `StreamingArchiveFile.h` (uses `ArchiveFile` as base class)
- Likely called by resource loading systems (e.g., W3D model loading, texture loading)

### Outgoing
- Uses `File` class (file I/O operations)
- Uses `ArchiveFileSystem` (for archive management)
- Uses `AsciiString` (string handling)

## Design Patterns
- **Abstract Factory**: `ArchiveFile` is an abstract base class that defines the interface for archive operations, with concrete implementations provided elsewhere (e.g., `StreamingArchiveFile`).
- **Composite**: Manages a directory tree structure (`DetailedArchivedDirectoryInfo`) to represent nested files within archives.
- **Dependency Injection**: The `attachFile` method allows external systems to inject file objects, decoupling archive management from file I/O.

(Not inferable: No clear use of other patterns like Observer or Strategy in this header alone.)
