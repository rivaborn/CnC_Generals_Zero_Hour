# Generals/Code/Libraries/Source/WWVegas/WWLib/TagBlock.h - Enhanced Analysis

## Architectural Role
This file defines the core infrastructure for the game's asset packaging system, enabling efficient storage and retrieval of game resources (models, textures, etc.) in a write-once/read-many format. It bridges the low-level file I/O (RawFileClass) with higher-level asset management systems.

## Cross-References
### Incoming
- Asset loading systems (e.g., W3D model loader)
- Modding infrastructure (custom asset handling)
- Save/load game functionality

### Outgoing
- RawFileClass for file operations
- SList for index management
- CRC calculations for integrity checks

## Design Patterns
- **Handle/Body Pattern**: TagBlockHandle provides controlled access to TagBlockFile's resources
- **Resource Pooling**: IndexList maintains sorted block references for efficient lookup
- **Write-Once/Read-Many**: Enforces data integrity through controlled write access

*Not inferable*: Specific usage patterns in game systems (e.g., streaming priorities)
