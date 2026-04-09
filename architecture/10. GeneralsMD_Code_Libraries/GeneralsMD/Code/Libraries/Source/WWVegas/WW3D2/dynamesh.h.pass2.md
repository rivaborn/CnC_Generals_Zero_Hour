# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/dynamesh.h - Enhanced Analysis

## Architectural Role
This file defines the dynamic mesh subsystem, a critical component for runtime geometry manipulation in the SAGE engine. It bridges low-level mesh geometry (MeshGeometryClass) with high-level rendering (RenderObjClass), enabling effects like particle systems, damage decals, and UI elements that require frequent geometry updates.

## Cross-References
### Incoming
- **Particle systems**: Call `DynamicMeshClass::Location()` and `End_Vertex()` for particle positioning
- **Damage system**: Uses `DynamicScreenMeshClass` for decal rendering
- **UI rendering**: Leverages `DynamicScreenMeshClass` for HUD elements
- **Shader system**: References `ShaderClass` for material assignment

### Outgoing
- **Mesh geometry**: Inherits from `MeshGeometryClass`, uses its vertex/polygon arrays
- **Material system**: Depends on `MeshMatDescClass` for texture/shader management
- **Rendering pipeline**: Integrates with `RenderInfoClass` for scene rendering
- **Math utilities**: Uses `Vector3/4/2` for vertex data

## Design Patterns
- **Composite**: `DynamicMeshClass` contains `DynamicMeshModel` (geometry) and `MeshMatDescClass` (materials)
- **Flyweight**: Reuses material/texture arrays across multiple dynamic meshes via `MaterialInfoClass`
- **Strategy**: Triangle rendering mode (strips/fans) can be switched at runtime via `TriMode`
