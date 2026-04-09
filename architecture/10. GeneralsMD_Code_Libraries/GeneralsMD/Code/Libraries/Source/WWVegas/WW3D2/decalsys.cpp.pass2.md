# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/decalsys.cpp - Enhanced Analysis

## Architectural Role
This file implements the decal management system, bridging the rendering pipeline (WW3D2) with game object interactions. It handles dynamic decal placement (e.g., bullet impacts, explosions) by managing decal generators and their association with meshes, ensuring decals are properly tracked and cleaned up.

## Cross-References
### Incoming
- **Rendering System**: Calls `DecalGeneratorClass::Add_Mesh` to register meshes for decal application.
- **Game Logic**: Uses `DecalSystemClass::Lock_Decal_Generator`/`Unlock_Decal_Generator` to create/destroy decals during events (e.g., weapon hits).
- **Resource Management**: Relies on `MultiFixedPoolDecalSystemClass` for memory pooling of decals.

### Outgoing
- **Memory Allocation**: Uses `W3DNEW`/`W3DNEWARRAY` for decal generator and pool management.
- **Mesh System**: Interacts with `MeshClass` via `NonRefRenderObjListIterator` for decal mesh tracking.
- **ID Generation**: Manages global decal IDs via `DecalIDGenerator`.

## Design Patterns
- **Object Pool Pattern**: `MultiFixedPoolDecalSystemClass` pre-allocates decal slots to avoid runtime allocation overhead.
- **Flyweight Pattern**: Decals are shared across meshes (e.g., same bullet hole texture reused).
- **Observer Pattern**: Meshes notify the decal system when destroyed via `Decal_Mesh_Destroyed` to clean up references.
