# Generals/Code/Libraries/Source/WWVegas/WW3D2/hrawanim.cpp - Enhanced Analysis

## Architectural Role
This file implements the core animation system for the W3D engine, handling hierarchical skeletal animations. It bridges between the low-level W3D file format and the runtime animation system, providing frame interpolation and motion channel access.

## Cross-References
### Incoming
- Animation playback systems (likely in WW3D2)
- Object rendering pipeline (uses Get_Transform)
- Visibility culling (uses Get_Visibility)

### Outgoing
- Motion channel system (motchan.h)
- W3D file I/O (chunkio.h)
- Asset management (assetmgr.h)
- Hierarchy system (htree.h)

## Design Patterns
- **Resource Management**: Uses explicit allocation/deallocation with Free() pattern
- **Data Accessor**: Provides controlled access to animation data via Get_* methods
- **Composite**: Manages collections of motion channels per node (NodeMotion array)

Key insight: The file shows tight coupling between animation data and hierarchy nodes, suggesting animations are node-specific rather than object-wide. The interpolation logic (Get_Transform) handles both translation and rotation separately before combining them, indicating a component-based animation system.
