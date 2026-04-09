# Generals/Code/Libraries/Source/WWVegas/WW3D2/projector.h - Enhanced Analysis

## Architectural Role
This file defines the core projection abstraction in the WW3D2 rendering subsystem, serving as a base class for texture projection and decal generation. It bridges the transformation pipeline with spatial queries, critical for both static and dynamic 3D rendering features.

## Cross-References
### Incoming
- `TexProjectClass` (texture projection system)
- `DecalGeneratorClass` (decal rendering)
- Rendering pipeline stages requiring projection matrices

### Outgoing
- `Matrix3D`, `Matrix4` (math library)
- `AABoxClass`, `OBBoxClass` (bounding volume system)
- `MatrixMapperClass` (internal projection mapping)

## Design Patterns
- **Template Method**: `Update_WS_Bounding_Volume()` as a virtual hook for derived classes
- **Composite**: Manages both local and world-space bounding volumes
- **Strategy**: Encapsulates projection type (perspective/ortho) as configurable behavior

*Not inferable: Exact inheritance hierarchy or `MatrixMapperClass` implementation details.*
