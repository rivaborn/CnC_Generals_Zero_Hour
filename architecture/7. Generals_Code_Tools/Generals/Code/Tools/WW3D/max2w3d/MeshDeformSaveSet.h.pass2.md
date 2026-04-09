# Generals/Code/Tools/WW3D/max2w3d/MeshDeformSaveSet.h - Enhanced Analysis

## Architectural Role
This file defines the core data structure for storing mesh deformation animations in the 3DS Max exporter toolchain. It bridges the Max plugin layer with the W3D asset pipeline, handling vertex-level animation data serialization.

## Cross-References
### Incoming
- `MeshDeformSaveClass` (friend class) - Uses this class to manage deformation data export
- Max plugin exporter code - Likely calls `Begin_Keyframe`/`Add_Vert` during animation baking

### Outgoing
- `DynamicVectorClass` - Uses for container storage of deformation data
- `ChunkSaveClass` (forward declared) - Likely used for binary serialization in the exporter

## Design Patterns
- **Composite Pattern**: `KEYFRAME` contains a `DynamicVectorClass<DEFORM_DATA>` to represent hierarchical deformation data
- **State Pattern**: Keyframe management via `Begin_Keyframe`/`End_Keyframe` suggests state-based animation handling
- **Flyweight Pattern**: Vertex data reuse via `vert_index` references rather than storing full vertex data

*Not inferable*: No clear use of Observer or Visitor patterns in this header-only definition.
