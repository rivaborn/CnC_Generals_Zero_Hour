# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/RAWFILE.H - Enhanced Analysis

## Architectural Role
This file defines the low-level file I/O abstraction layer (`RawFileClass`) that bridges platform-specific file operations (Windows/Unix) with the higher-level `FileClass` hierarchy. It serves as the foundational I/O component for asset loading, save/load operations, and modding infrastructure.

## Cross-References
### Incoming
- **Asset loading systems** (e.g., W3D model loader, INI parsers)
- **Save/load game logic** (serialization of game state)
- **Modding tools** (file access for custom content)
- **Derived file classes** (e.g., packed files, CD-ROM support)

### Outgoing
- **Platform-specific APIs** (Windows `HANDLE`, Unix `FILE*`)
- **Error handling** (custom `Error` method, potentially linked to `WWERROR` macros)
- **String utilities** (`wwstring.h` for filename management)

## Design Patterns
- **Adapter Pattern**: Abstracts platform-specific file I/O behind a unified interface.
- **Template Method**: Defines virtual methods (`Open`, `Read`, `Write`) for derived classes to override.
- **Biasing Mechanism**: Implements a sub-file access pattern (e.g., for multi-part files like mixfiles).

*Not inferable*: Exact inheritance chain or usage of `FileClass` hierarchy.
