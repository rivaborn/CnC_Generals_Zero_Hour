# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/rinfo.h - Enhanced Analysis

## Architectural Role
This file defines the core rendering state container (`RenderInfoClass`) that bridges the scene graph and the rendering pipeline in the WW3D engine. It encapsulates camera, lighting, and material state while providing mechanisms for temporary overrides and special rendering modes.

## Cross-References
### Incoming
- Rendering pipeline components (e.g., `SceneClass`, `ObjectClass`) likely instantiate and populate `RenderInfoClass` before rendering.
- Material system (`MaterialPassClass`) implementations call `Push_Material_Pass` to register additional render passes.
- Shadow/visibility systems use `SpecialRenderInfoClass` for specialized rendering.

### Outgoing
- Relies on `CameraClass` for view/culling state.
- Interfaces with `LightEnvironmentClass` for lighting data.
- Uses `VisRasterizerClass` and `BWRenderClass` for special rendering modes (visibility detection/shadows).

## Design Patterns
- **State Container**: `RenderInfoClass` acts as a parameter object carrying render state through the pipeline.
- **Stack-Based Overrides**: Uses a stack pattern for `OverrideFlag` to allow nested temporary state changes (e.g., for shadows).
- **Template Method Variant**: `SpecialRenderInfoClass` extends the base class for specialized rendering, avoiding pollution of the main pipeline.
