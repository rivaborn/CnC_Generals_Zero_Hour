# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/matrixmapper.h - Enhanced Analysis

## Architectural Role
This file defines the core texture coordinate mapping system for the W3D2 rendering pipeline, enabling projected textures and composite mappings. It bridges the gap between world-space transformations and texture-space coordinates, critical for effects like shadow mapping and environment projections.

## Cross-References
### Incoming
- Rendering pipeline (e.g., `TexProjectClass` mentioned in comments)
- Shader stages (via `stage` parameter in constructor)
- Texture coordinate generation (callers of `Apply` and `Compute_Texture_Coordinate`)

### Outgoing
- `TextureMapperClass` (base class)
- `Matrix4x4`, `Matrix3D`, `Vector3` (math utilities)
- `Mapper.h` (parent interface)

## Design Patterns
- **Template Method**: `Apply` and `Calculate_Texture_Matrix` define hooks for subclasses to customize texture matrix computation.
- **Composite**: `CompositeMatrixMapperClass` delegates to an internal mapper, enabling recursive texture transformations.
- **Strategy**: Different `MappingType` enums allow runtime selection of projection algorithms (ortho/perspective/gradient).

*Not inferable*: Exact callers of `Apply` or `Compute_Texture_Coordinate` (would require tracing render pipeline).
