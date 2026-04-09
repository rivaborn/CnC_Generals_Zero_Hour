# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/decalsys.h - Enhanced Analysis

## Architectural Role
This file defines the core decal system architecture in the SAGE engine, bridging rendering and scene management. It provides the interface for dynamic decal generation on 3D objects, with special handling for translucent meshes and backface culling.

## Cross-References
### Incoming
- Rendering pipeline (calls `DecalGeneratorClass::Add_Mesh` when creating decals)
- Scene management (uses `DecalSystemClass::Lock_Decal_Generator` for decal creation)
- Material system (references `MaterialPassClass` for decal materials)

### Outgoing
- Projector system (inherits from `ProjectorClass`)
- Memory management (uses `NonRefRenderObjListClass` for mesh tracking)
- ID generation (static `DecalIDGenerator` counter)

## Design Patterns
- **Factory Pattern**: `DecalSystemClass` manages creation/release of `DecalGeneratorClass` instances
- **Composite Pattern**: `MultiFixedPoolDecalSystemClass` uses nested `LogicalDecalPoolClass` and `LogicalDecalClass` for hierarchical decal management
- **Observer Pattern**: Meshes register themselves with generators via `Add_Mesh` for later cleanup

*Not inferable*: Exact relationship with W3D rendering pipeline or how decal IDs map to GPU resources.
