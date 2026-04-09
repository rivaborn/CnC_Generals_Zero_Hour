# GeneralsMD/Code/GameEngine/Source/Common/System/LocalFile.cpp - Enhanced Analysis

## Architectural Role
This file implements the low-level filesystem abstraction layer for the SAGE engine, bridging between the abstract `File` interface and platform-specific I/O operations. It's a critical dependency for all subsystems requiring persistent storage access.

## Cross-References
### Incoming
- Game logic (loading/saving game data)
- AI (reading behavior scripts)
- W3D (loading 3D assets)
- UI (loading interface assets)
- Modding infrastructure (file access for mods)

### Outgoing
- `RAMFile` (for memory-mapped file operations)
- Platform-specific I/O functions (`fopen`, `_open`, etc.)
- `PerfTimer` (for performance measurement)

## Design Patterns
- **Adapter Pattern**: Wraps platform-specific I/O functions behind a unified interface
- **Resource Tracking**: Uses `s_totalOpen` to monitor open file handles (debugging aid)
- **Factory Pattern**: `convertToRAMFile()` creates `RAMFile` instances dynamically

*Not inferable*: Exact usage patterns in higher-level subsystems (e.g., async loading).
