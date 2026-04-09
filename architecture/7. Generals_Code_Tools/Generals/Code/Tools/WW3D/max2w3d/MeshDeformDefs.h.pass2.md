# Generals/Code/Tools/WW3D/max2w3d/MeshDeformDefs.h - Enhanced Analysis

## Architectural Role
This header defines core data structures for mesh deformation in the 3DS Max to W3D exporter tool, bridging between Max's SDK and the engine's W3D format requirements. It serves as the type system for vertex manipulation operations during model export.

## Cross-References
### Incoming
- Likely used by `MeshDeform.cpp` (deformation processing logic)
- Referenced by other max2w3d exporter modules handling vertex data

### Outgoing
- Uses `DynamicVectorClass` from Max SDK (container)
- Relies on `Point3` from local `Vector.H` (math)

## Design Patterns
- **Data Transfer Object (DTO)**: `VERT_INFO` encapsulates vertex data for export
- **Type Object**: `DEFORM_CHANNELS` enum defines deformation capabilities
- **Template Method**: `DynamicVectorClass` usage suggests deferred iteration logic

*Not inferable*: No clear strategy/observer patterns visible in this header-only file.
