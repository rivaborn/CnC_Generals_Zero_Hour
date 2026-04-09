# Generals/Code/Libraries/Source/WWVegas/WW3D2/decalmsh.h - Enhanced Analysis

## Architectural Role
This file defines the decal system's core classes, bridging the rendering pipeline (WW3D) with the game's dynamic object interactions. It abstracts decal management for both static and skinned meshes, enabling effects like bullet holes or explosion marks.

## Cross-References
### Incoming
- Likely called by `MeshClass` (parent mesh) and `DecalSystemClass` (manager)
- Used by rendering subsystems when applying decals to objects

### Outgoing
- Depends on `ShaderClass`, `TextureClass`, and `VertexMaterialClass` for material handling
- Uses `SimpleDynVecClass` for dynamic array management (memory subsystem)

## Design Patterns
- **Template Method**: Abstract `DecalMeshClass` defines interface, concrete classes implement behavior
- **Composite**: `DecalMeshClass` maintains linked list (`NextVisible`) for visibility culling
- **Strategy**: Different decal types (rigid/skin) encapsulated in separate classes

*Not inferable*: Exact relationship with `DecalGeneratorClass` or `OBBoxClass` usage.
