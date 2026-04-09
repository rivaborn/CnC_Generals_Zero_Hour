# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/pointgr.h

## Purpose
Defines classes for rendering point-based graphics (e.g., particle systems) in the SAGE engine.

## Responsibilities
- Manages point group rendering with configurable modes (tris, quads, screenspace)
- Handles point attributes (position, color, size, orientation, frame)
- Supports texture mapping and shaders for points
- Provides billboarding and transformation options
- Optimizes rendering with precomputed vertex/UV tables

## Key Types
- **PointGroupClass (Class)**: Main class for rendering point groups (particles).
- **PointModeEnum (Enum)**: Point rendering modes (TRIS, QUADS, SCREENSPACE).
- **FlagsType (Enum)**: Operation flags (TRANSFORM).
- **SegmentGroupClass (Class)**: Subclass of PointGroupClass (likely for line segments).

## Key Functions
### `Set_Arrays`
- Purpose: Sets point attribute arrays (locations, colors, sizes, etc.).
- Calls: `Update_Arrays`

### `Render`
- Purpose: Renders the point group using provided render info.
- Calls: `Update_Arrays` (indirectly via internal logic)

### `Update_Arrays`
- Purpose: Updates internal arrays for rendering.
- Calls: None (internal helper)

## Globals
- **`_TriVertexLocationOrientationTable` (Vector3[256][3])**: Precomputed vertex locations for triangle mode.
- **`_QuadVertexLocationOrientationTable` (Vector3[256][4])**: Precomputed vertex locations for quad mode.
- **`PointMaterial` (VertexMaterialClass*)**: Shared material for points.

## Dependencies
- `sharebuf.h`, `shader.h`, `vector4.h`, `vector3.h`, `vector2.h`, `vector.h`
- `VertexMaterialClass`, `RenderInfoClass`, `TextureClass` (forward declarations)
