# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/textdraw.h - Enhanced Analysis

## Architectural Role
This file defines the `TextDrawClass`, a core component of the SAGE engine's 2D rendering system. It bridges the 3D rendering pipeline (via `DynamicMeshClass`) with the UI and HUD systems by providing screen-space text and primitive rendering capabilities.

## Cross-References
### Incoming
- **UI/HUD Systems**: Likely call `Print()` methods for in-game text rendering (score, unit stats, etc.)
- **Debug Rendering**: Uses `Line()` and `Quad()` for diagnostic overlays
- **Font Management**: External `Font3DInstanceClass` is passed in for text rendering

### Outgoing
- **Rendering Pipeline**: Inherits from `DynamicMeshClass` for vertex/polygon management
- **Math Utilities**: Uses `Vector2`, `Vector3`, and `RectClass` for coordinate transformations
- **Shader System**: References `VertexMaterialClass` and `ShaderClass` for material setup

## Design Patterns
- **Template Method**: `Reset()` and coordinate transformation methods define hooks for derived classes
- **Composite**: Aggregates `DynamicMeshClass` functionality while adding text-specific behavior
- **Strategy**: Font rendering behavior is delegated to external `Font3DInstanceClass` instances

*Not inferable: Exact usage patterns of `CLASSID_TEXTDRAW` or dynamic mesh management.*
