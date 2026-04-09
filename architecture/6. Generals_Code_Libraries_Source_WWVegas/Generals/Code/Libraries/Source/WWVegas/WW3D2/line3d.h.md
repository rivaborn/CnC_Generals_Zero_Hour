# Generals/Code/Libraries/Source/WWVegas/WW3D2/line3d.h

## Purpose
Defines the `Line3DClass` for rendering 3D line segments in the game engine.

## Responsibilities
- Render 3D line segments as cylinders with configurable width.
- Manage line properties (position, color, opacity, sorting).
- Provide bounding volume calculations for collision/visibility.

## Key Types
- **Line3DClass (Class)**: Renders 3D line segments with configurable width and color.
- **VertexMaterialClass (Class)**: Forward declaration (material handling).
- **RenderInfoClass (Class)**: Forward declaration (rendering context).
- **None**: No enums/structs defined.

## Key Functions
### `Line3DClass(const Vector3 & start, const Vector3 & end, float width, float r, float g, float b, float opacity)`
- Purpose: Constructs a 3D line segment.
- Calls: Not inferable (constructor body not shown).

### `Render(RenderInfoClass & rfinfo)`
- Purpose: Renders the line segment.
- Calls: Not inferable (implementation in .cpp).

### `Scale(float scale)`
- Purpose: Scales the line symmetrically about its center.
- Calls: Not inferable.

### `Reset(const Vector3 & new_start, const Vector3 & new_end)`
- Purpose: Updates the line's start/end points.
- Calls: Not inferable.

## Globals
- **None**: No global/static variables.

## Dependencies
- `rendobj.h` (base class `RenderObjClass`)
- `vector3.h`, `vector4.h` (math types)
- `shader.h` (shader handling)
- `always.h` (likely macros/asserts)
