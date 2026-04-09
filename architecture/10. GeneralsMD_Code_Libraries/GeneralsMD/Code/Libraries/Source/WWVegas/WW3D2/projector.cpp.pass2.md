# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/projector.cpp - Enhanced Analysis

## Architectural Role
This file implements the `ProjectorClass`, a core component of the SAGE engine's 3D rendering pipeline. It handles projection transformations and texture coordinate calculations, bridging the gap between world-space geometry and screen-space rendering.

## Cross-References
### Incoming
- Rendering subsystem (likely calls `Compute_Texture_Coordinate` for dynamic lighting/shadow mapping)
- Camera system (uses `Set_Transform` for projector positioning)
- Scene graph (relies on `Update_WS_Bounding_Volume` for culling)

### Outgoing
- `MatrixMapperClass` (delegates texture coordinate calculations)
- `OBBoxClass` (for bounding volume transformations)
- `Matrix3D`/`Vector3` (core math types)

## Design Patterns
- **Strategy Pattern**: Uses `MatrixMapperClass` to encapsulate different projection calculation strategies (perspective/orthographic)
- **Composite Pattern**: Manages local/world-space bounding volumes as part of a larger spatial hierarchy
- **Observer Pattern**: Implicitly notifies dependent systems (e.g., renderers) when projections change via bounding volume updates

*Not inferable*: Exact usage patterns in lighting/shadow systems remain unclear from this file alone.
