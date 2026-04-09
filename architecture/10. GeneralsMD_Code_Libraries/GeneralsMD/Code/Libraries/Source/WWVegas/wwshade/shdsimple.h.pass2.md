# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shdsimple.h - Enhanced Analysis

## Architectural Role
This file defines the basic shader system for the SAGE engine, bridging shader definitions (`ShdSimpleDefClass`) with runtime implementations (`Shd6SimpleClass`). It handles simple textured rendering with ambient/diffuse lighting, serving as a foundational component for the rendering pipeline.

## Cross-References
### Incoming
- Rendering subsystem calls `Shd6SimpleClass::Apply_Shared` and `Apply_Instance` during scene rendering
- Shader factory uses `ShdSimpleDefClass::Create` to instantiate shaders

### Outgoing
- Calls into `TextureClass` for texture management
- Uses `D3DMATERIAL8` for Direct3D material state
- Relies on `Matrix4x4` for view/projection transformations

## Design Patterns
- **Factory Pattern**: `ShdSimpleDefClass::Create` instantiates shader implementations
- **Strategy Pattern**: Shader behavior is encapsulated in separate classes (`Shd6SimpleClass`) for different APIs
- **Property Pattern**: Ambient/diffuse properties are exposed via getter/setter methods for configuration

*Not inferable*: Exact usage of `View_Projection_Matrix` in rendering pipeline.
