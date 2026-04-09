# Generals/Code/Tools/WW3D/max2w3d/MeshDeformData.h - Enhanced Analysis

## Architectural Role
This file defines the core data structure for mesh deformation in the 3DS Max plugin toolchain, bridging the gap between Max's modifier system and the W3D export pipeline. It encapsulates deformation state management, critical for skeletal animation and vertex morphing in the game's W3D format.

## Cross-References
### Incoming
- `Generals/Code/Tools/WW3D/max2w3d/MeshDeformMod.cpp` (implementation file)
- `Generals/Code/Tools/WW3D/max2w3d/MeshDeformSet.cpp` (uses `MeshDeformSetClass` methods)
- 3DS Max plugin system (calls `LocalModData` virtual methods)

### Outgoing
- `MeshDeformSet.H` (delegates deformation operations)
- `<Max.h>` (3DS Max SDK for `TriObject`, `Mesh` access)
- `Vector.H` (dynamic array management)

## Design Patterns
- **Adapter Pattern**: Wraps 3DS Max's `LocalModData` to expose deformation-specific functionality.
- **Composite Pattern**: Manages a collection of `MeshDeformSetClass` objects as a single unit (`SETS_LIST`).
- **State Pattern**: Implicitly tracks mesh states via `Record_Mesh_State` and `Restore_Set` for deformation history.

*Not inferable*: Exact serialization format for `Save`/`Load` or threading considerations.
