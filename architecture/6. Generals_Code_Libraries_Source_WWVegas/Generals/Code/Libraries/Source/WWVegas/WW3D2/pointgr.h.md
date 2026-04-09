# Generals/Code/Libraries/Source/WWVegas/WW3D2/pointgr.h

## Purpose
Defines classes for rendering point-based graphics (e.g., particle systems) in the SAGE engine.

## Responsibilities
- Manages point groups with customizable rendering properties (size, color, orientation, etc.)
- Handles point mode (triangles, quads, screen-space)
- Provides texture and shader support for points
- Supports billboarding and transformation flags
- Optimizes rendering with precomputed vertex/UV tables

## Key Types
- **PointGroupClass (Class)**: Core class for rendering point groups (particles).
- **PointModeEnum (Enum)**: Point rendering mode (TRIS, QUADS, SCREENSPACE).
- **FlagsType (Enum)**: Operation control flags (e.g., TRANSFORM).
- **SegmentGroupClass (Class)**: Subclass of PointGroupClass (likely for line segments).
- **VertexMaterialClass (Class)**: External material class reference.
- **RenderInfoClass (Class)**: External render info class reference.
- **TextureClass (Class)**: External texture class reference.

## Key Functions
### `Set_Arrays`
- Purpose: Sets point location, color, and other arrays for rendering.
- Calls: `Update_Arrays`

### `Render`
- Purpose: Renders the point group using the provided render info.
- Calls: `Update_Arrays` (indirectly via internal logic)

### `Update_Arrays`
- Purpose: Updates internal arrays for rendering (compresses data, applies transformations).
- Calls: None (internal helper)

### `_Init` / `_Shutdown`
- Purpose: Initializes/shuts down static vertex/UV tables.
- Calls: None (static initialization)

## Globals
- **`_TriVertexLocationOrientationTable` (Vector3[256][3])**: Precomputed vertex positions for triangle mode.
- **`_QuadVertexLocationOrientationTable` (Vector3[256][4])**: Precomputed vertex positions for quad mode.
- **`_ScreenspaceVertexLocationSizeTable` (Vector3[2][3])**: Precomputed vertex positions for screen-space mode.
- **`_TriVertexUVFrameTable` / `_QuadVertexUVFrameTable` (Vector2*)**: Precomputed UV coordinates for frames.
- **`PointMaterial` (VertexMaterialClass*)**: Static material for points.

## Dependencies
- **Includes**: `sharebuf.h`, `shader.h`, `vector4.h`, `vector3.h`, `vector2.h`, `vector.h`
- **External Classes**: `VertexMaterialClass`, `RenderInfoClass`, `TextureClass`, `ShaderClass`
- **External Types**: `Vector3`, `Vector4`, `Vector2`
