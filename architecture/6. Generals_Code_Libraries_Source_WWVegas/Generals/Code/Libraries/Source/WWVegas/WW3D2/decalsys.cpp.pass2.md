# Generals/Code/Libraries/Source/WWVegas/WW3D2/decalsys.cpp - Enhanced Analysis

## Architectural Role
This file implements the decal management subsystem within the WW3D2 rendering pipeline, handling dynamic surface projections (e.g., bullet holes, scorch marks) that must persist across frames while being tied to specific mesh instances. It bridges the gap between static geometry and runtime effects, with special handling for object destruction cleanup.

## Cross-References
### Incoming
- **Rendering Pipeline**: `MeshClass` objects call into `DecalGeneratorClass::Add_Mesh` during effect application
- **Game Logic**: Destruction events trigger `MultiFixedPoolDecalSystemClass::Decal_Mesh_Destroyed` via mesh parent relationships
- **Resource Management**: `W3DNEW`/`W3DNEWARRAY` allocations are tracked by the engine's memory system

### Outgoing
- **Render Objects**: Directly manipulates `MeshClass` decal lists via `Delete_Decal`
- **Material System**: Relies on `SurfaceClass`/`MaterialPassClass` for texture projection (included headers)
- **WW3D Core**: Uses `MatrixMapperClass` for coordinate space transformations

## Design Patterns
- **Object Pool Pattern**: `MultiFixedPoolDecalSystemClass` pre-allocates decal slots to avoid runtime allocation during intense combat scenarios
- **Flyweight Pattern**: Decal definitions are shared while instances are tracked per mesh via `LogicalDecalClass`
- **Observer Pattern**: Mesh destruction notifies the decal system to clean up references (implicit via parent relationship)

*Not inferable*: Exact texture projection implementation details or how decals interact with dynamic lighting.
