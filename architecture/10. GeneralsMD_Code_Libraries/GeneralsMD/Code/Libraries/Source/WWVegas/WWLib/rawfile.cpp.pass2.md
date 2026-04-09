# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/rawfile.cpp - Enhanced Analysis

## Architectural Role
This file implements the core file I/O abstraction layer (`RawFileClass`) used throughout the SAGE engine. It provides cross-platform file operations with biasing support, serving as the foundation for asset loading, save/load systems, and modding infrastructure.

## Cross-References
### Incoming
- Game logic modules (e.g., mission loading, save/load)
- Asset management systems (W3D model loading, texture loading)
- Modding infrastructure (custom asset handling)
- Networking code (file transfers, patching)

### Outgoing
- Platform-specific APIs (Windows/Unix file operations)
- Error handling system (`Error` function)
- String manipulation utilities (`StringClass`)

## Design Patterns
- **Wrapper Facade**: Abstracts platform-specific file operations behind a unified interface
- **Resource Management**: Handles file handles with `Attach`/`Detach` for shared access scenarios
- **Biasing Pattern**: Implements virtual sub-file ranges for memory-mapped or embedded file handling

*Not inferable*: Specific usage patterns in game logic or networking layers.
