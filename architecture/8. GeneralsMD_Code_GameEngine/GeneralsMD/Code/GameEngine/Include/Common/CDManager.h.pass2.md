# GeneralsMD/Code/GameEngine/Include/Common/CDManager.h - Enhanced Analysis

## Architectural Role
This file defines the CD-ROM management subsystem, bridging the game's disk verification system with the underlying hardware abstraction layer. It provides a platform-agnostic interface for detecting game disks, critical for copy protection and content validation in the SAGE engine.

## Cross-References
### Incoming
- Likely called by:
  - Copy protection/anti-piracy systems (e.g., disk verification)
  - Main game initialization (to validate game disks at startup)
  - Mod loading systems (to check for valid expansion content)

### Outgoing
- Depends on:
  - `SubSystemInterface` for engine subsystem integration
  - `List.h` for drive management (linked list pattern)
  - Platform-specific CD-ROM drivers (not shown in header)

## Design Patterns
- **Interface-Based Abstraction**: Uses `CDDriveInterface` and `CDManagerInterface` to decouple CD-ROM operations from concrete implementations, enabling platform-specific backends.
- **Singleton-like Global Access**: `TheCDManager` provides a global point of access, though creation is delegated to `CreateCDManager()` (Factory Method).
- **Composite Pattern**: `CDManager` aggregates multiple `CDDrive` instances in a list, treating them as a unified collection.

*Not inferable*: No clear Observer pattern for disk changes (though `refreshDrives()` suggests potential callbacks).
