# GeneralsMD/Code/GameEngine/Source/Common/System/ArchiveFileSystem.cpp - Enhanced Analysis

## Architectural Role
This file implements the virtual file system layer that abstracts access to game assets stored in BIG archive files. It bridges the gap between the game's resource loading needs and the physical file system, enabling mod support and efficient asset management.

## Cross-References
### Incoming
- Game logic subsystems (e.g., W3D model loading, audio asset loading)
- Mod loading infrastructure (via `loadMods`)
- Resource management systems (via `openFile` and `doesFileExist`)

### Outgoing
- `ArchiveFile` class for actual file operations
- `AsciiString` for path manipulation
- `TheGlobalData` for mod configuration

## Design Patterns
- **Singleton**: Global `TheArchiveFileSystem` instance provides centralized access
- **Composite**: Directory tree structure (`ArchivedDirectoryInfo`) organizes files hierarchically
- **Strategy**: Different archive files can be loaded with varying priorities (mods vs. base game)

Not inferable: No clear use of Factory, Observer, or other patterns in the visible code.
