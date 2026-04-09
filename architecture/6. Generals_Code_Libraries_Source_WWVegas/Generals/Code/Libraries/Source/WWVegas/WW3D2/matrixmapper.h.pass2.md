# Generals/Code/Libraries/Source/WWVegas/WW3D2/matrixmapper.h - Enhanced Analysis

## Architectural Role
This file defines the `MatrixMapperClass`, a core component of the SAGE engine's rendering pipeline responsible for texture coordinate computation in projected textures. It bridges the gap between world-space transformations and texture-space mapping, critical for effects like decals, shadows, and environment mapping.

## Cross-References
### Incoming
- **Rendering Pipeline**: Likely called by shader stages or material systems to compute texture coordinates.
- **Texture Management**: Used by texture projection systems (e.g., `TexProjectClass` mentioned in comments).
- **Effect Systems**: Potentially referenced by particle systems or post-processing effects requiring dynamic texture mapping.

### Outgoing
- **Math Library**: Relies on `Matrix3D`, `Matrix4`, and `Vector3` for transformations.
- **Texture System**: Interfaces with `TextureMapperClass` (base class) for texture coordinate generation.
- **DirectX 8**: Uses DX8 texture matrices (noted in comments), indicating tight integration with the graphics API layer.

## Design Patterns
- **Template Method**: `Apply(int uv_array_index)` is virtual, suggesting subclasses implement specific texture mapping logic.
- **Strategy**: Different `MappingType` enums allow runtime selection of projection strategies (ortho/perspective/gradient).
- **Dependency Injection**: `Set_Texture_Transform` injects transformation matrices, decoupling coordinate computation from the caller.
