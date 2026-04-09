# Generals/Code/Libraries/Source/WWVegas/WW3D2/decalsys.h - Enhanced Analysis

## Architectural Role
This file defines the core decal system architecture, bridging the rendering pipeline (WW3D2) with game-specific decal behavior. It manages decal lifecycle, spatial queries, and material application, serving as the central interface for decal operations in the SAGE engine.

## Cross-References
### Incoming
- Rendering subsystem calls `DecalGeneratorClass::Add_Mesh` when meshes generate decals
- Game logic calls `DecalSystemClass::Lock_Decal_Generator`/`Unlock_Decal_Generator` for decal creation
- Scene management uses `MultiFixedPoolDecalSystemClass::Clear_Decal_Slot` for decal cleanup

### Outgoing
- Depends on `ProjectorClass` for decal projection math
- Uses `MaterialPassClass` for decal material properties
- Interacts with `RenderObjClass` for mesh decal application

## Design Patterns
- **Factory Pattern**: `DecalSystemClass` manages creation/release of `DecalGeneratorClass` instances
- **Observer Pattern**: `DecalGeneratorClass` tracks meshes via `MeshList` for later cleanup
- **Composite Pattern**: `MultiFixedPoolDecalSystemClass` organizes decals into hierarchical pools/slots
