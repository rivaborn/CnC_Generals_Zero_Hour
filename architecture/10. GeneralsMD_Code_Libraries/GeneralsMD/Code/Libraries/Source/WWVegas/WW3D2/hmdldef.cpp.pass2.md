# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/hmdldef.cpp - Enhanced Analysis

## Architectural Role
This file implements the core hierarchical model loading system for the W3D renderer. It bridges between the file I/O subsystem (ChunkLoadClass) and the rendering pipeline by parsing W3D hierarchical model definitions and managing their memory lifecycle.

## Cross-References
### Incoming
- Rendering system (likely calls Load_W3D during asset initialization)
- Animation system (uses SubObjects array for bone hierarchy)
- Physics system (references SnapPoints for attachment points)

### Outgoing
- Chunk I/O subsystem (uses ChunkLoadClass for file parsing)
- Memory management (W3DNEW/W3DNEWARRAY macros)
- SnapPoints system (creates SnapPointsClass instances)

## Design Patterns
- **Resource Management**: Uses explicit Free() pattern with RAII-style destructor
- **Composite**: Models hierarchical relationships through SubObjects array
- **Version Adapter**: Handles pre-3.0 W3D format compatibility via conditional logic

*Not inferable*: Factory pattern usage or observer relationships to other systems.
