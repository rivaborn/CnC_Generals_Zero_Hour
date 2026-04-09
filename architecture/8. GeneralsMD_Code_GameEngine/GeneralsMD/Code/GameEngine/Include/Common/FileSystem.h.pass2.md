# GeneralsMD/Code/GameEngine/Include/Common/FileSystem.h - Enhanced Analysis

## Architectural Role
This file defines the core file system abstraction layer, bridging the engine's I/O needs with platform-specific implementations (e.g., LocalFileSystem, ArchiveFileSystem). It centralizes asset path management and provides a unified interface for file operations across subsystems.

## Cross-References
### Incoming
- **LocalFileSystem.h/ArchiveFileSystem.h**: Implement FileSystem interface methods (openFile, doesFileExist, etc.)
- **Asset loading subsystems**: W3D model loader, texture manager, INI parser
- **Modding infrastructure**: Custom asset path resolution

### Outgoing
- **STL containers**: Uses std::map for file existence caching
- **SubsystemInterface**: Inherits for engine initialization lifecycle
- **File.h**: Forward reference for file handle creation

## Design Patterns
- **Abstract Factory**: FileSystem creates concrete File objects (e.g., LocalFile, ArchiveFile)
- **Singleton**: Global TheFileSystem instance ensures single file system access point
- **Cache-Aside**: m_fileExist map caches file existence checks for performance

*Not inferable*: No clear use of Observer or Strategy patterns in this header.
