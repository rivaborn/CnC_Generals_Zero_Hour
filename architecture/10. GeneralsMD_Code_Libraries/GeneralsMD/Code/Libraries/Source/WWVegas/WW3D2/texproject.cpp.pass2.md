# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/texproject.cpp - Enhanced Analysis

## Architectural Role
This file implements the texture projection system for the SAGE engine, serving as the core component for dynamic lighting and shadow effects. It bridges the rendering pipeline with material management, handling both perspective and orthographic projections for real-time texture generation.

## Cross-References
### Incoming
- **Rendering Pipeline**: `WW3D::Begin_Render`, `WW3D::Render`, `WW3D::End_Render` (called during texture generation)
- **Material System**: `MaterialPassClass` methods (used for shader configuration)
- **Camera System**: `CameraClass` (configured for projection rendering)

### Outgoing
- **DX8 Wrapper**: `DX8Wrapper::Set_Render_Target_With_Z` (for render target management)
- **Asset Management**: `AssetManagerClass` (for texture loading)
- **Culling System**: `Set_Cull_Box` (for spatial partitioning)

## Design Patterns
- **Strategy Pattern**: Projection type (perspective/orthographic) is encapsulated in separate methods (`Compute_Perspective_Projection`, `Compute_Ortho_Projection`).
- **Observer Pattern**: Intensity interpolation updates are frame-time dependent (`WW3D::Get_Frame_Time`).
- **Composite Pattern**: Texture projection is part of a larger rendering hierarchy (inherits from `ProjectorClass`).

**Note**: Shadow mapping math comments reveal deep integration with the engine's transformation pipeline.
