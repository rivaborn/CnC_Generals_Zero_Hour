# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/texproject.h - Enhanced Analysis

## Architectural Role
This file defines the core texture projection system for the SAGE engine, enabling dynamic lighting effects (e.g., shadows) and decals. It bridges the rendering pipeline (WW3D2) with the scene graph and culling system, supporting both static and dynamic projections.

## Cross-References
### Incoming
- **Rendering System**: Uses `MaterialPassClass` and `MatrixMapperClass` for shader/matrix setup.
- **Scene Graph**: Integrates with `RenderObjClass` for projection target management.
- **Culling System**: Inherits `CullableClass` for frustum culling.

### Outgoing
- **Texture Management**: Depends on `TextureClass` and `ZTextureClass` for render targets.
- **Projection Math**: Uses `ProjectorClass` and `CameraClass` for view frustum calculations.
- **List System**: Leverages `MultiListClass` for efficient scene graph traversal.

## Design Patterns
- **Strategy Pattern**: Projection type (perspective/ortho) is encapsulated in separate methods (`Set_Perspective_Projection`, `Set_Ortho_Projection`).
- **Observer Pattern**: `Pre_Render_Update` suggests this class reacts to camera changes (likely via scene graph notifications).
- **Composite Pattern**: `TexProjListClass` aggregates projectors, enabling batch operations (e.g., culling).

*Not inferable*: Exact inheritance hierarchy of derived classes (e.g., `DynTexProjectClass`).
