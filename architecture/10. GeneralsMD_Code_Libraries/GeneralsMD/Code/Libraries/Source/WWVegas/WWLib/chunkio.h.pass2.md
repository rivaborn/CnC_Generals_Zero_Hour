# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/chunkio.h - Enhanced Analysis

## Architectural Role
This file defines the core chunk-based file I/O system used throughout the engine for serialization of game assets (W3D models, INI files) and save games. It provides hierarchical chunking with versioning support via micro-chunks, enabling forward/backward compatibility for file formats.

## Cross-References
### Incoming
- W3D model loading/saving pipeline (`GeneralsMD/Code/Libraries/Source/WWVegas/W3D/...`)
- INI file serialization (`GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/ini.h`)
- Save game system (`GeneralsMD/Code/Game/.../savegame.cpp`)

### Outgoing
- File I/O operations (`wwfile.h`)
- Memory management (`iostruct.h` for vector/quaternion serialization)
- Error handling (`always.h` for assertions)

## Design Patterns
- **Facade Pattern**: Hides complex chunk navigation behind simple `Begin_Chunk`/`End_Chunk` methods
- **Composite Pattern**: Hierarchical chunk structure allows recursive nesting of data
- **Template Method**: Macros like `WRITE_MICRO_CHUNK` provide consistent serialization patterns
